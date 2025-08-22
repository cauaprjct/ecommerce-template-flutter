# 🤝 Contribuindo para o E-commerce Template Flutter

Obrigado por considerar contribuir para este projeto! Sua ajuda é muito bem-vinda.

## 📋 Como Contribuir

### 🐛 Reportando Bugs

1. Verifique se o bug já foi reportado nas [Issues](https://github.com/cauaprjct/ecommerce-template-flutter/issues)
2. Se não encontrar, crie uma nova issue com:
   - Título claro e descritivo
   - Descrição detalhada do problema
   - Passos para reproduzir o bug
   - Comportamento esperado vs atual
   - Screenshots (se aplicável)
   - Informações do ambiente (Flutter version, OS, etc.)

### 💡 Sugerindo Melhorias

1. Abra uma issue com a tag `enhancement`
2. Descreva claramente a melhoria proposta
3. Explique por que seria útil para o projeto
4. Inclua exemplos de uso, se possível

### 🔧 Contribuindo com Código

#### Pré-requisitos
- Flutter SDK 3.8.1+
- Dart SDK 3.8.0+
- Git
- Editor de código (VS Code, Android Studio, etc.)

#### Processo de Desenvolvimento

1. **Fork** o repositório
2. **Clone** seu fork:
   ```bash
   git clone https://github.com/seu-usuario/ecommerce-template-flutter.git
   cd ecommerce-template-flutter
   ```

3. **Crie uma branch** para sua feature:
   ```bash
   git checkout -b feature/nome-da-feature
   ```

4. **Instale as dependências**:
   ```bash
   flutter pub get
   ```

5. **Faça suas alterações** seguindo os padrões do projeto

6. **Teste suas alterações**:
   ```bash
   flutter test
   flutter analyze
   ```

7. **Commit suas mudanças**:
   ```bash
   git add .
   git commit -m "feat: adiciona nova funcionalidade"
   ```

8. **Push para sua branch**:
   ```bash
   git push origin feature/nome-da-feature
   ```

9. **Abra um Pull Request**

## 📝 Padrões de Código

### Estrutura de Arquivos
- Siga a estrutura Clean Architecture existente
- Um arquivo por classe
- Nome do arquivo igual ao nome da classe (snake_case)

### Nomenclatura
- **Classes**: PascalCase (`ProductModel`, `GetAllProducts`)
- **Arquivos**: snake_case (`product_model.dart`, `get_all_products.dart`)
- **Variáveis**: camelCase (`productList`, `isLoading`)
- **Constantes**: UPPER_SNAKE_CASE (`API_BASE_URL`)

### Comentários
- Use comentários em português
- Documente classes e métodos públicos
- Explique lógicas complexas

### Commits
Use [Conventional Commits](https://www.conventionalcommits.org/):
- `feat:` nova funcionalidade
- `fix:` correção de bug
- `docs:` documentação
- `style:` formatação
- `refactor:` refatoração
- `test:` testes
- `chore:` tarefas de manutenção

## 🧪 Testes

- Escreva testes para novas funcionalidades
- Mantenha cobertura de testes alta
- Execute `flutter test` antes de fazer commit

## 📖 Documentação

- Atualize o README se necessário
- Documente novas APIs ou mudanças significativas
- Mantenha os exemplos atualizados

## ❓ Dúvidas

Se tiver dúvidas sobre como contribuir:
1. Verifique a documentação existente
2. Procure em issues fechadas
3. Abra uma nova issue com a tag `question`

## 🎉 Reconhecimento

Todos os contribuidores serão reconhecidos no README do projeto.

---

**Obrigado por contribuir! 🚀**