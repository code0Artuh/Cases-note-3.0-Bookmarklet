 Cases Notes 3.0 - Documentação

 Elementos Reutilizáveis

 1. `homeCasesElement`
   - Representa o elemento da página inicial para casos.

 2. `buttonCreateWriteCard`
   - Botão para adicionar notas e e-mails aos casos.

 3. `dataCase`
   - Variável que contém os dados do caso.

 4. `speakeasyIDCase`
   - Array que armazena IDs do Speakeasy.

 Coleção de Eventos Reutilizáveis

 1. `bubbleEventClick`
   - Evento de clique com bolhas ativadas.

 2. `bubbleEventFocus`
   - Evento de foco com bolhas ativadas.

 3. `bubbleEventBlur`
   - Evento de desfoque com bolhas ativadas.

 4. `bubbleEventInput`
   - Evento de entrada com bolhas ativadas.

 Funções de Teste no Console

 1. `consoleText(text)`
   - Exibe uma mensagem grande e colorida no console (fundo branco, texto preto).

 2. `consoleSuccess(text)`
   - Exibe uma mensagem de sucesso no console (fundo verde, texto amarelo).

 3. `consoleAlert(text)`
   - Exibe uma mensagem de alerta no console (fundo amarelo, texto vermelho).

 4. `consoleError(text)`
   - Exibe uma mensagem de erro no console (fundo vermelho, texto amarelo).

 Função para Formatação de Data

 1. `formatData()`
   - Retorna uma string no formato "dd/mm/aaaa" correspondente à data atual.

 Função para Criação de Estilo CSS

 1. `createStyle(atributo)`
   - Cria um elemento `<link>` para incluir uma folha de estilo CSS no cabeçalho da página.

 Função para Movimentação de Elemento

 1. `dragElement(elemento)`
   - Permite arrastar um elemento na página utilizando eventos do mouse.

 Função para Redimensionamento de Elemento

 1. `resizeWindow(elemento)`
   - Adiciona um redimensionador ao elemento fornecido, permitindo que seja redimensionado pelo usuário com eventos do mouse.

 Função para Exibição de Conteúdo de Acordo com a Aba Selecionada

 1. `handleTabClick(tabId)`
   - Trata a exibição do conteúdo correspondente à aba selecionada.
   - Passos:
      1. Remove a classe 'highlight' de todos os botões de abas.
      2. Adiciona a classe 'highlight' ao botão da aba selecionada.
      3. Esconde todo o conteúdo exibido anteriormente.
      4. Exibe o conteúdo correspondente à aba selecionada.

 Função para Criação de Popup

 1. `createPopup(contentPopUp)`
   - Cria um popup com o conteúdo fornecido.
   - Composto por uma div pai (`popupDivFather`) e uma div filho (`popupDiv`).
   - Adiciona um botão de fechamento ao popup e define um ouvinte de evento para remover o popup ao clicar no botão de fechamento.
   - O conteúdo do popup é inserido na div filho.
   - A div pai é adicionada ao elemento com o ID "notes".

 Função para Exibição do Popup

 1. `showPopup(data)`
   - Exibe um popup obtendo o conteúdo de um arquivo HTML específico, com base no parâmetro `data` fornecido.
   - Realiza uma requisição assíncrona usando o método `fetch` para obter o conteúdo do arquivo HTML.
   - Se o conteúdo obtido contém o identificador "id="popup-important"", a função chama `createPopup(contentPopUp)` para criar e exibir o popup.

 Função para Resetar Campos de Input, Textarea e Select

 1. `resetFields()`
   - Reseta os campos de input, textarea e select dentro do elemento com o ID "notes".
   - Para cada elemento encontrado, a função identifica o tipo do elemento e realiza a ação apropriada para efetuar o reset, limpando valores ou desmarcando checkboxes e radio buttons.

 Função para Definir o Conteúdo do Elemento com o ID "hotkey-agendamento"

 1. `setHotkeyValue(value)`
   - Define o conteúdo do elemento com o ID "hotkey-agendamento" com o valor `value` passado como argumento.

 Função para Lidar com a Mudança no Elemento com o ID "substatus-agendamento"

 1. `handleSubstatusChange(e)`
   - Lida com a mudança no elemento com o ID "substatus-agendamento".
   - Chamada quando ocorre uma mudança no valor do elemento e recebe o evento `e` como argumento.
   - Obtém o valor selecionado, chama `setHotkeyValue(selectedValue)` para definir o conteúdo do elemento com o ID "hotkey-agendamento" com o valor selecionado e exibe uma mensagem no console indicando a alteração do substatus.

 Função para Observar Mudanças no DOM e Chamar o Callback Quando um Novo Elemento é Adicionado

 1. `observeChanges(callback)`
   - Observa as mudanças no DOM e chama o `callback` quando um novo elemento é adicionado.
   - Retorna uma Promise que é resolvida com o MutationObserver para futura manipulação.
   - Recebe o `callback` como argumento, que será chamado quando um novo elemento for adicionado ao DOM.
   - O `callback` recebe o novo elemento adicionado e o próprio MutationObserver como argumentos.

 Função Recursiva para Verificar se um Elemento ou Seus Descendentes Contêm um Texto Específico ou um Elemento com o Seletor Fornecido

 1. `checkElements(element, targetTextOrSelector)`
   - Chamada recursiva para verificar se um elemento ou algum de seus descendentes contêm o texto específico ou um elemento com o seletor fornecido.
   - Retorna `true` se o elemento ou descendente for encontrado e `false` caso contrário.

 Função para Realizar Ação Quando um Elemento com Texto Específico ou Seletor Fornecido é Adicionado ao DOM

 1. `actionChanges(targetTextOrSelector, callback)`
   - Responsável por realizar a ação quando um elemento com o texto específico ou seletor fornecido é adicionado ao DOM.
   - Retorna uma Promise resolvida com o elemento encontrado.
   - Recebe o `targetTextOrSelector` como primeiro argumento e

 o `callback` como segundo argumento.
   - Utiliza a função `observeChanges(callback)` para observar as mudanças no DOM e chamar o `callback` quando um novo elemento é adicionado.

 Função para Lidar com a Mudança no Elemento com o ID "status-agendamento"

 1. `handleStatusChange(e)`
   - Lida com a mudança no elemento com o ID "status-agendamento".
   - Chamada quando ocorre uma mudança no valor do elemento e recebe o evento `e` como argumento.
   - Chama a função `actionChanges` para realizar a ação quando um elemento com o texto específico ou seletor fornecido é adicionado ao DOM.

 Função para Lidar com a Mudança no Elemento com o ID "prioridade-agendamento"

 1. `handlePriorityChange(e)`
   - Lida com a mudança no elemento com o ID "prioridade-agendamento".
   - Chamada quando ocorre uma mudança no valor do elemento e recebe o evento `e` como argumento.
   - Chama a função `actionChanges` para realizar a ação quando um elemento com o texto específico ou seletor fornecido é adicionado ao DOM.

 Função para Lidar com a Mudança no Elemento com o ID "hotkey-agendamento"

 1. `handleHotkeyChange(e)`
   - Lida com a mudança no elemento com o ID "hotkey-agendamento".
   - Chamada quando ocorre uma mudança no valor do elemento e recebe o evento `e` como argumento.
   - Exibe uma mensagem no console indicando a alteração da tecla de atalho.

 Função para Adicionar um Evento de Clique a um Elemento com um Seletor Específico

 1. `addClickEvent(selector, callback)`
   - Adiciona um evento de clique a um elemento com o seletor específico.
   - Retorna uma Promise resolvida com o elemento alvo.
   - Recebe o `selector` como primeiro argumento e o `callback` como segundo argumento.
   - Utiliza a função `actionChanges` para realizar a ação quando um elemento com o seletor fornecido é adicionado ao DOM.

 Função para Lidar com a Mudança no Elemento com o ID "pacote-agendamento"

 1. `handlePackageChange(e)`
   - Lida com a mudança no elemento com o ID "pacote-agendamento".
   - Chamada quando ocorre uma mudança no valor do elemento e recebe o evento `e` como argumento.
   - Exibe uma mensagem no console indicando a alteração do pacote.

 Função para Atualizar as Opções de Seleção com Base nos Dados Fornecidos

 1. `updateSelectOptions(selectId, options)`
   - Atualiza as opções de um elemento de seleção com base nos dados fornecidos.
   - Recebe o `selectId` como primeiro argumento, que é o ID do elemento de seleção a ser atualizado.
   - Recebe o `options` como segundo argumento, que é um array de opções a serem adicionadas ao elemento de seleção.

 Função para Atualizar a Lista de Pacotes com Base nos Dados Fornecidos

 1. `updatePackageList(packages)`
   - Atualiza a lista de pacotes com base nos dados fornecidos.
   - Recebe o `packages` como argumento, que é um array de objetos representando os pacotes.
   - Para cada pacote, a função cria um elemento de lista (`<li>`) contendo o nome do pacote e a quantidade de casos associados a ele.
   - Remove todas as entradas anteriores na lista de pacotes e adiciona as novas entradas criadas.

 Função para Lidar com a Mudança no Elemento com o ID "solicitante-agendamento"

 1. `handleRequesterChange(e)`
   - Lida com a mudança no elemento com o ID "solicitante-agendamento".
   - Chamada quando ocorre uma mudança no valor do elemento e recebe o evento `e` como argumento.
   - Exibe uma mensagem no console indicando a alteração do solicitante.

 Função para Adicionar Estilo CSS ao Documento

 1. `addCSSStyles(styles)`
   - Adiciona estilos CSS ao documento.
   - Recebe o `styles` como argumento, que é um objeto contendo pares chave-valor representando propriedades e valores CSS.
   - Cria uma tag `<style>` e adiciona as regras de estilo ao conteúdo da tag.
   - Adiciona a tag `<style>` ao cabeçalho do documento.

 Função para Adicionar Estilos Específicos do Componente

 1. `addComponentStyles()`
   - Adiciona estilos específicos do componente ao documento.
   - Utiliza a função `addCSSStyles(styles)` para adicionar os estilos específicos.

 Função para Adicionar Eventos aos Elementos do DOM

 1. `addDOMEvents()`
   - Adiciona eventos aos elementos do DOM.
   - Utiliza a função `addClickEvent(selector, callback)` para adicionar eventos de clique a elementos específicos do DOM.

 Função para Obter os Dados do Caso Atual

 1. `getCurrentCaseData()`
   - Obtém os dados do caso atual.
   - Utiliza o elemento com o ID "current-case" para obter os dados do caso atual.

 Função para Inicializar o Componente de Casos

 1. `initCasesComponent()`
   - Inicializa o componente de casos.
   - Utiliza as funções `addComponentStyles()`, `addDOMEvents()`, `getCurrentCaseData()`, e outras funções específicas para configurar e adicionar estilos, eventos e interatividade ao componente.

Este é um guia abrangente das funções, elementos e eventos reutilizáveis no componente de casos. Consulte este documento para referência durante o desenvolvimento e manutenção do componente.


