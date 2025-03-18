# CardView

## Descrição

Este projeto é responsável por exibir as cartas de cada jogador em um jogo de cartas de Pokémon. A aplicação consulta serviços de distribuição de cartas e de jogadores para recuperar as informações necessárias sobre os jogadores e suas cartas. Além disso, a aplicação consulta a PokéAPI para recuperar as informações necessárias sobre os Pokémons.

## Funcionalidades

- **Consulta de Jogadores:** Recupera informações sobre os jogadores.
- **Consulta de Cartas:** Consulta o serviço de distribuição de cartas para obter as cartas de cada jogador.
- **Consulta de Pokémons:** Utiliza a PokéAPI para obter informações detalhadas sobre os Pokémons nas cartas.
- **Exibição de Cartas:** Exibe as cartas de cada jogador com as informações obtidas.

## Tecnologias Utilizadas
- **Front-end:** React
- **APIs:** PokéAPI

## UML
### Fluxograma
<img src="https://github.com/user-attachments/assets/ffb4ca04-b769-47bd-adac-81d9d1393c70" width="600">

#### Descrição  
O fluxograma descreve o funcionamento da tela do jogo, desde o início até a interação do usuário e a atualização da interface.

#### Explicação do Fluxograma  

- **Inicialização**: O jogo começa com o **carregamento de recursos** e a **configuração das interfaces**.  
- **Carregamento dos Dados**: O sistema verifica se os dados foram carregados corretamente.  
  - Se **SIM**, o processo segue para a renderização.  
  - Se **NÃO**, o sistema tenta **obter os dados das cartas**. Caso falhe, uma **mensagem de erro** é exibida.  
- **Renderização e Interação**: Se os dados foram carregados corretamente, a **tela é renderizada** e a **interatividade é ativada**.  
- **Loop de Interação**: O sistema monitora a interação do usuário:  
  - Se houver interação, a **tela é atualizada**.  
  - Caso contrário, o sistema **aguarda uma ação**.  
  - O sistema verifica se o usuário deseja sair:  
    - Se **SIM**, o jogo termina.  
    - Se **NÃO**, o loop continua.  

#### Conclusão  
O fluxograma garante uma **interação contínua** e uma **experiência de jogo fluida**, assegurando o carregamento correto dos recursos e o tratamento adequado de erros. Dessa forma, o sistema mantém uma interface responsiva e funcional.

### Diagrama de Caso de Uso  
<img src="https://github.com/user-attachments/assets/a5c73fc2-cfff-4615-8634-dd59d7a43714" width="600">

#### Descrição  
O diagrama de caso de uso representa o fluxo de visualização de cartas no jogo, descrevendo como o jogador interage com o sistema para acessar suas cartas.

#### Fluxo do Processo


1. O **jogador** acessa a **Tela de Cadastro/Login** e entra no sistema.  
2. Após o cadastro, ele recebe **5 Pokémon aleatórios** da funcionalidade **"Distribuição de Cartas"**.  
3. O jogador solicita a funcionalidade **"Exibir Cartas"**.  
4. O sistema consulta os serviços necessários:  
   - **Serviço de Jogadores** para obter informações sobre o jogador.  
   - **Serviço de Distribuição de Cartas** para recuperar os Pokémon atuais no deck do jogador.  
   - **PokéAPI** para obter os detalhes dos Pokémon no deck do jogador.  

Com todas as informações recuperadas, as **cartas são exibidas** ao jogador na interface do .  

#### Conclusão  
O diagrama ilustra a interação entre o jogador e os serviços do , garantindo que as cartas sejam carregadas corretamente e exibidas de forma dinâmica e responsiva.  

### Diagrama de Classe  
<img src="https://github.com/user-attachments/assets/53398ea0-f7fc-42b0-98ef-0cb416a2a720" width="600">  

#### Descrição  
O diagrama de classes representa a estrutura da aplicação que exibe as cartas dos jogadores, detalhando as classes principais e seus relacionamentos.  

#### Estrutura do Sistema  

- **Aplicação de Visualização de Cartas**: Classe principal que coordena a recuperação e exibição dos dados dos jogadores e suas cartas.  
- **Jogador**: Representa um jogador no sistema, contendo nome e uma lista de Pokémon recuperada da **PokéAPI**.  
- **Carta**: Representa uma carta pertencente a um jogador, sendo fornecida pelo **Serviço de Distribuição de Cartas**.  

#### Relacionamento com os Serviços  

- **Serviço de Jogadores**: Fornece informações sobre o jogador.  
- **Serviço de Distribuição de Cartas**: Responsável pelas cartas associadas ao jogador.  
- **PokéAPI**: Recupera detalhes dos Pokémon em formato JSON.  

#### Conclusão  
O diagrama de classes organiza e define claramente as responsabilidades de cada classe no sistema, facilitando a compreensão e a integração entre os diferentes componentes. Ele permite uma manutenção mais eficiente e uma expansão do sistema de forma modular e escalável.  
 


