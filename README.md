<div align="center">

# 🛒 E-commerce Template Flutter

### Template completo de e-commerce com Clean Architecture

[![Flutter](https://img.shields.io/badge/Flutter-3.8.1+-02569B?style=for-the-badge&logo=flutter&logoColor=white)](https://flutter.dev)
[![Dart](https://img.shields.io/badge/Dart-3.8.0+-0175C2?style=for-the-badge&logo=dart&logoColor=white)](https://dart.dev)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=for-the-badge)](CONTRIBUTING.md)

**Um template profissional de e-commerce desenvolvido em Flutter seguindo os princípios da Clean Architecture. Pronto para produção e fácil de personalizar.**

[🚀 Demo](#-demo) • [📱 Features](#-features) • [🛠️ Instalação](#️-instalação) • [📖 Documentação](#-documentação) • [🤝 Contribuir](#-contribuindo)

---

</div>

## 🚀 Demo

> **Nota:** Screenshots e demo em breve!

<!--
Adicione aqui screenshots do seu app:
![Home Screen](screenshots/home.png)
![Products Screen](screenshots/products.png)
![Cart Screen](screenshots/cart.png)
-->

## ✨ Features

### ✅ **Implementado**
- 🏗️ **Clean Architecture** com separação clara de responsabilidades
- 🎯 **BLoC Pattern** para gerenciamento de estado reativo
- 📦 **Repository Pattern** para abstração de dados
- 🔄 **Cache inteligente** com Hive para performance offline
- 🌐 **Integração com APIs** REST com tratamento de erros
- 🎨 **UI/UX moderna** com Material Design 3
- 📱 **Design responsivo** para mobile, tablet e web
- 🔍 **Sistema de busca** em tempo real
- 🛒 **Catálogo de produtos** com grid adaptativo
- ⚡ **Hot reload** e desenvolvimento ágil

### 🔄 **Roadmap**
- 🛒 Carrinho de compras completo
- 🔐 Autenticação com Firebase
- ❤️ Sistema de favoritos
- 👤 Perfil do usuário
- 💳 Integração com pagamentos
- 📊 Dashboard administrativo
- 🔔 Push notifications
- 🌙 Tema escuro

## 🛠️ Tecnologias Utilizadas

### Core
- **Flutter** 3.8.1+
- **Dart** 3.8.0+

### Gerenciamento de Estado
- **flutter_bloc** ^9.1.1
- **equatable** ^2.0.7

### Networking & Data
- **dio** ^5.9.0
- **hive** ^2.2.3
- **hive_flutter** ^1.1.0
- **cached_network_image** ^3.4.1

### Funcional Programming
- **dartz** ^0.10.1

### Firebase (Opcional)
- **firebase_core** ^4.0.0
- **firebase_auth** ^6.0.1
- **cloud_firestore** ^6.0.0

### Navegação
- **go_router** ^16.2.0

### Utilitários
- **shared_preferences** ^2.5.3

## 📁 Estrutura do Projeto

```
lib/
├── core/                          # Funcionalidades compartilhadas
│   ├── constants/                 # Constantes da aplicação
│   ├── errors/                    # Classes de erro
│   ├── network/                   # Configuração de rede
│   ├── usecases/                  # Use cases base
│   └── utils/                     # Utilitários
├── features/                      # Features da aplicação
│   ├── auth/                      # Autenticação
│   │   ├── data/
│   │   ├── domain/
│   │   └── presentation/
│   ├── cart/                      # Carrinho de compras
│   │   ├── data/
│   │   ├── domain/
│   │   └── presentation/
│   ├── products/                  # Produtos
│   │   ├── data/
│   │   │   ├── datasources/       # Fontes de dados
│   │   │   ├── models/            # Models para serialização
│   │   │   └── repositories/      # Implementação dos repositories
│   │   ├── domain/
│   │   │   ├── entities/          # Entidades de negócio
│   │   │   ├── repositories/      # Contratos dos repositories
│   │   │   └── usecases/          # Casos de uso
│   │   └── presentation/
│   │       ├── bloc/              # BLoCs para gerenciamento de estado
│   │       ├── pages/             # Páginas da aplicação
│   │       └── widgets/           # Widgets reutilizáveis
│   └── user/                      # Usuário
│       ├── data/
│       ├── domain/
│       └── presentation/
└── shared/                        # Recursos compartilhados
    ├── themes/                    # Temas da aplicação
    └── widgets/                   # Widgets globais
```

## 🚀 Início Rápido

### Pré-requisitos
- Flutter SDK 3.8.1+
- Dart SDK 3.8.0+
- Android Studio / VS Code
- Git

### Instalação

1. **Clone o repositório**
```bash
git clone https://github.com/cauaprjct/ecommerce-template-flutter.git
cd ecommerce-template-flutter
```

2. **Instale as dependências**
```bash
flutter pub get
```

3. **Execute o projeto**
```bash
# Para desenvolvimento
flutter run

# Para web
flutter run -d chrome

# Para build de produção
flutter build apk --release
```

### 🎯 Comandos Úteis

```bash
# Análise de código
flutter analyze

# Testes
flutter test

# Formatação
dart format .

# Build para diferentes plataformas
flutter build apk --release      # Android
flutter build ios --release      # iOS
flutter build web --release      # Web
```

### Configuração Adicional

#### Firebase (Opcional)
Para usar as funcionalidades do Firebase:

1. Crie um projeto no [Firebase Console](https://console.firebase.google.com/)
2. Configure o projeto para Android/iOS
3. Baixe os arquivos de configuração:
   - `google-services.json` (Android) → `android/app/`
   - `GoogleService-Info.plist` (iOS) → `ios/Runner/`

#### API Externa
O template usa a [Fake Store API](https://fakestoreapi.com/) por padrão. Para usar sua própria API:

1. Edite `lib/core/constants/api_constants.dart`
2. Atualize a `baseUrl` e endpoints conforme necessário
3. Ajuste os models em `lib/features/products/data/models/`

## 🧪 Testes

```bash
# Executar todos os testes
flutter test

# Executar testes com coverage
flutter test --coverage

# Gerar relatório de coverage
genhtml coverage/lcov.info -o coverage/html
```

## 📖 Guia de Desenvolvimento

### Adicionando uma Nova Feature

1. **Crie a estrutura de pastas**
```
lib/features/nova_feature/
├── data/
│   ├── datasources/
│   ├── models/
│   └── repositories/
├── domain/
│   ├── entities/
│   ├── repositories/
│   └── usecases/
└── presentation/
    ├── bloc/
    ├── pages/
    └── widgets/
```

2. **Implemente seguindo a Clean Architecture**
   - Comece pelas **Entities** (domain/entities)
   - Defina os **Repository contracts** (domain/repositories)
   - Crie os **Use Cases** (domain/usecases)
   - Implemente os **Models** (data/models)
   - Crie os **Data Sources** (data/datasources)
   - Implemente o **Repository** (data/repositories)
   - Desenvolva o **BLoC** (presentation/bloc)
   - Construa as **Pages** e **Widgets** (presentation/)

### Padrões de Código

#### Nomenclatura
- **Classes**: PascalCase (`ProductModel`, `GetAllProducts`)
- **Arquivos**: snake_case (`product_model.dart`, `get_all_products.dart`)
- **Variáveis**: camelCase (`productList`, `isLoading`)
- **Constantes**: UPPER_SNAKE_CASE (`API_BASE_URL`)

#### Estrutura de Arquivos
- Um arquivo por classe
- Nome do arquivo igual ao nome da classe principal
- Imports organizados: Flutter → Packages → Relative

#### Comentários
- Use comentários em português
- Documente classes e métodos públicos
- Explique lógicas complexas

## 🤝 Contribuindo

1. Fork o projeto
2. Crie uma branch para sua feature (`git checkout -b feature/nova-feature`)
3. Commit suas mudanças (`git commit -m 'Adiciona nova feature'`)
4. Push para a branch (`git push origin feature/nova-feature`)
5. Abra um Pull Request

### Diretrizes de Contribuição
- Siga os padrões de código estabelecidos
- Adicione testes para novas funcionalidades
- Atualize a documentação quando necessário
- Use commits semânticos

## 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

## 🙏 Agradecimentos

- [Flutter Team](https://flutter.dev/) pelo framework incrível
- [Fake Store API](https://fakestoreapi.com/) pelos dados de exemplo
- Comunidade Flutter pelo suporte e recursos

## 📞 Suporte

Se você encontrar algum problema ou tiver dúvidas:

1. Verifique as [Issues existentes](https://github.com/cauaprjct/ecommerce-template-flutter/issues)
2. Crie uma nova issue se necessário
3. Consulte a [documentação do Flutter](https://docs.flutter.dev/)

---

**Desenvolvido por Cauã usando Flutter**
