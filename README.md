# WeatherApp

WeatherApp é um aplicativo desenvolvido em React Native com Expo, que utiliza a API WeatherAPI para exibir dados da previsão do tempo de diferentes cidades.

## Bibliotecas Utilizadas

- **@expo-google-fonts/nunito**: Para carregar e utilizar a fonte "Nunito" no aplicativo.
- **@react-native-async-storage/async-storage**: Para armazenamento local de dados (não utilizado para cache no momento).
- **@react-navigation/native & @react-navigation/native-stack**: Para navegação entre as telas do app.
- **axios**: Utilizado para fazer as requisições HTTP à API WeatherAPI.
- **dayjs**: Biblioteca para manipulação de datas.
- **expo**: Framework para desenvolvimento com React Native.
- **expo-font**: Gerencia as fontes carregadas no app.
- **expo-location**: Utilizado para acessar a localização do dispositivo, permitindo que o usuário veja a previsão do tempo com base em sua localização atual.
- **expo-status-bar**: Gerencia a barra de status do dispositivo.
- **react-native-safe-area-context**: Garante que o layout do app respeite as áreas seguras do dispositivo (como a barra de status).
- **react-native-screens**: Melhora o desempenho da navegação, utilizando views nativas.
- **react-native-svg**: Para renderizar imagens em SVG no app.
- **react-native-toast-message**: Para exibir mensagens de erro e feedback ao usuário.
- **jest & jest-expo**: Ferramentas de teste automatizado.

## Requisitos para Executar o Projeto

1. **Clonar o repositório**:
   ```bash
   git clone https://github.com/Gilnavarro1/WeatherApp.git
   cd weatherapp
   ```

2. **Instalar as dependências**:
   Certifique-se de ter o Node.js instalado e execute:
   ```bash
   npm install
   ```

3. **Configurar a chave da API**:
   Crie um arquivo `.env` na raiz do projeto com a sua chave da API WeatherAPI:
   ```
   EXPO_PUBLIC_WEATHER_APP_ID=your_api_key
   ```

4. **Instalar o plugin `expo-location`** (se necessário):
   Caso o plugin não esteja instalado automaticamente, utilize o seguinte comando para instalá-lo:
   ```bash
   npx expo install expo-location
   ```
   Esse plugin é usado para acessar a localização do dispositivo. O app solicitará permissão ao usuário para obter a localização sempre e enquanto o aplicativo estiver em uso, conforme a configuração abaixo:
   ```json
   {
     "plugins": [
       [
         "expo-location",
         {
           "locationAlwaysAndWhenInUsePermission": "Allow $(PRODUCT_NAME) to use your location."
         }
       ],
       "expo-font"
     ]
   }
   ```

5. **Executar o aplicativo**:
   Inicie o Expo:
   ```bash
   npm start
   ```

6. **Testar o aplicativo em um emulador ou dispositivo físico**:
   Siga as instruções do Expo para rodar no Android ou iOS.

## Observações

- **Testes em dispositivos Apple**: O aplicativo foi testado apenas em dispositivos Apple. Não houve a oportunidade de testar em dispositivos Android durante o desenvolvimento.
- **Tratamento de Erros**: O app atualmente não possui tratamentos robustos para cenários de falha de conexão ou problemas na resposta da API.

## Comentários Adicionais

- O aplicativo foi desenvolvido sem o uso de cache para os dados da previsão do tempo. Isso significa que sempre que o usuário solicitar os dados do clima, uma nova requisição à API será feita.
  
---
