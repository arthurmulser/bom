
# bom

bitcoin offline minemonic.

## Estrutura de Pastas do Projeto - 20260524

```
lib/
├── constants.dart                          # constantes globais da aplicação;
├── main.dart                               # ponto de entrada da aplicação;
└── src/
    ├── algorithms/                         # algoritmos diversos;
    ├── screens/                            # telas iniciais do projeto;
    ├── services/                           # serviços;
    │   ├── api/                            # apis externas;
    │   └── interfaces/                     # contratos/interfaces dos serviços;
    ├── shared/                             # componentes e funções compartilhadas;
    └── mvvm_lars/                          # arquitetura mvvm;
        ├── a_models/                       # modelo de dados;
        ├── b_database/                     # dados persistentes;
        │   ├── database_schema.dart        # nomes das colunas;
        │   ├── database_service.dart       # padrão singleton;
        │   ├── migrations/                 # migrações;
        │   └── repository/                 # padrão repository;
        ├── c_view/                         # componentes de ui;
        └── d_viewmodels/                   # lógica de negócio;
```

---

## Árvore das Telas (em ordem alfabética)

```
main
├── login
│   └── menu
└── menu
    ├── logout
    │   └── login
    ├── menu btc
    │   ├── cotação btc
    │   ├── endereços btc
    │   └── saldo btc
    ├── menu sc
    ├── qr code
    │   └── scan qr code
    └── setup
        └── tabelas sqlite
```

---

## Descrição das Telas (em ordem alfabética)

| Tela | Caminho do Arquivo | Descrição |
| :--- | :--- | :--- |
| **BTCCotacaoView** | `lib/src/mvvm_lars/c_view/btc_cotacao_view.dart` | Consulta de preços históricos do Bitcoin. |
| **BTCEnderecosView** | `lib/src/mvvm_lars/c_view/btc_enderecos_view.dart` | Cadastro e listagem de endereços de carteira. |
| **BTCSaldoCarteiraView** | `lib/src/mvvm_lars/c_view/btc_saldo_carteira_view.dart` | Consulta de saldo de endereços públicos. |
| **LoginScreen** | `lib/src/screens/login_screen.dart` | Interface para autenticação do usuário. |
| **Mars32Screen** | `lib/main.dart` | Tela inicial que verifica o estado de login. |
| **MenuBTCScreen** | `lib/src/screens/menu_btc_screen.dart` | Submenu para funcionalidades relacionadas a Bitcoin. |
| **MenuSCScreen** | `lib/src/screens/menu_sc_screen.dart` | Funcionalidades específicas do módulo SC (Tarefas). |
| **MenuScreen** | `lib/src/screens/menu_screen.dart` | Hub principal de navegação do aplicativo. |
| **QrCodeScannerScreen** | `lib/src/screens/qr_code_scanner_screen.dart` | Leitura de códigos QR via câmera. |
| **SetupScreen** | `lib/src/screens/setup_screen.dart` | Opções de configuração e testes do sistema. |
| **SqliteScreen** | `lib/src/screens/sqlite_screen.dart` | Interface para depuração do banco de dados local. |
| **TextToQrCodeScreen** | `lib/src/screens/text_to_qrcode_screen.dart` | Conversão de texto em imagem QR Code. |

---

20251009 - created with: flutter create --org br.com.vedvoyager --platforms android,ios bom;