# Jardim Pessoal

Catálogo pessoal de plantas feito em Flutter para o trabalho final de **Desenvolvimento Mobile I**. O usuário cadastra suas plantas (nome, tipo, local, status e observações), consulta os detalhes e edita as informações.

## Escopo do M1

Implementado (tudo em memória, sem login nem serviço externo):

- lista de plantas com estado vazio;
- tela de detalhe da planta selecionada;
- formulário único para criar e editar, com validação;
- layout adaptável: lista simples em tela estreita; lista e painel de detalhe lado a lado em largura igual ou maior que 720;
- tema Material 3 verde, rótulos nos campos e tooltip no botão de adicionar;
- teste de widget e análise estática.

Fora do escopo (evoluções futuras): persistência em banco, notificações de lembrete de rega, busca e remoção de plantas.

## Requisitos

- Flutter estável com Dart `^3.13.5` (definido no `pubspec.yaml`).
- Android SDK instalado para gerar o APK. Nenhuma credencial ou serviço externo é necessário.

## Como executar

```bash
git clone <endereço do repositório>
cd personal_jardim
git checkout m1-entrega
flutter pub get
flutter analyze
flutter test
flutter run
```

Para gerar o APK: `flutter build apk --release`. O arquivo sai em `build/app/outputs/flutter-apk/app-release.apk`.

## Estrutura

```
lib/
  main.dart                  ponto de entrada e MaterialApp
  models/planta.dart         modelo Planta e opções dos campos
  theme/app_theme.dart       tema Material 3
  screens/                   lista_page, detalhe_page, formulario_page
  widgets/                   planta_card, planta_detalhe, estado_vazio
test/
  lista_page_test.dart       testes de widget
```

## Versão avaliada

Tag `m1-entrega`.
