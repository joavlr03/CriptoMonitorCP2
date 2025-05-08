
# 📱 Android Crypto Monitor

Aplicativo que monitora o valor de criptomoedas usando a API pública do [Mercado Bitcoin](https://www.mercadobitcoin.com.br/). Ele exibe informações de cotação atual, com opção de atualização via botão.

## 🚀 Funcionalidades

- Exibe o valor atual do Bitcoin (ou outra moeda configurável).
- Interface simples com botão de atualização.
- Consumo de API com Retrofit.

## 🧩 Componentes Importantes

### `TicketResponse.kt`
Representa o modelo de dados retornado pela API. Contém campos como:
- `high`, `low`: valor mais alto e mais baixo do dia.
- `last`: último preço negociado.
- `vol`: volume total negociado.

### `MercadoBitcoinService.kt`
Interface Retrofit que define os endpoints da API pública do Mercado Bitcoin. Exemplo:
```kotlin
@GET("api/BTC/ticker/")
suspend fun getBitcoinTicker(): TicketResponse
```

### `MainActivity.kt`
Controla a lógica da interface:
- Chama o `MercadoBitcoinService`.
- Atualiza a UI com os dados retornados.
- Gatilho para o botão de refresh.

## 🌐 Uso da API

A aplicação utiliza a API pública do Mercado Bitcoin:

```
GET https://www.mercadobitcoin.net/api/BTC/ticker/
```

Os dados são mapeados para a classe `TicketResponse.kt`.

## 📦 Dependências Principais

- [Retrofit](https://square.github.io/retrofit/) – consumo de APIs.
- [Kotlin Coroutines](https://kotlinlang.org/docs/coroutines-overview.html) – chamadas assíncronas.
- [Material Design Components](https://m3.material.io/) – UI moderna.

## ▶️ Como Executar

1. Clone o projeto:
```bash
git clone https://github.com/seuusuario/android-crypto-monitor.git
```
2. Abra no Android Studio.
3. Conecte um emulador ou dispositivo físico.
4. Clique em **Run** ▶️.

## 📷 Interface

- Tela principal exibe os valores atuais do Bitcoin.
- Botão “Atualizar” refaz a requisição à API.

## Telas 

1.Antes de Atualizar

![tela 1](<Captura de tela 2025-05-08 183626.png>)

2. Depois de atualizar 

![tela 2](<Captura de tela 2025-05-08 183633.png>)

