# Teste Técnico - Aplicação Full-Stack com Next.js, tRPC e Langchain

## Objetivo

Desenvolver uma aplicação full-stack simples utilizando Next.js, tRPC e Langchain, que permita ao usuário final interagir com uma Large Language Model (LLM). A aplicação deve possibilitar o envio de mensagens para a LLM, permitindo realizar alterações diretas e precisas em um objeto JSON denominado **source**. Este objeto representa a **"fonte da verdade"** e contém informações sobre o usuário final e seu negócio, sendo enriquecido ao longo das conversas.

## Persona

O usuário final é o proprietário de um negócio que busca uma ferramenta para gerenciar informações sobre sua empresa e obter insights valiosos por meio de interações com uma inteligência artificial, com o objetivo de tomar decisões estratégicas.

## Requisitos Mínimos

1. **Estrutura do Projeto**
   - Utilizar **Next.js** como o framework principal para o desenvolvimento full-stack, abrangendo tanto o frontend quanto o backend.
   - Implementar **tRPC** para garantir comunicação type-safe entre o cliente e o servidor, proporcionando uma arquitetura eficiente e escalável.
   - Recomenda-se utilizar o template disponível em [create.t3.gg](https://create.t3.gg/), que já oferece um ponto de partida para uma aplicação full-stack com Next.js e tRPC. Isso pode facilitar o desenvolvimento e permitir que o candidato concentre seus esforços nas funcionalidades essenciais do projeto.
   
2. **Interface de Usuário (UI)**
   - Desenvolver uma interface de chat simples e funcional para que o usuário possa interagir diretamente com a LLM.
   - Incluir um componente de visualização que exiba o conteúdo atualizado da **source** (um objeto JSON representando os dados do negócio), permitindo ao usuário acompanhar as alterações em tempo real.

3. **Integração com LLM**
   - Utilizar **Langchain** para gerenciar a comunicação com a LLM, mantendo o contexto das interações e garantindo respostas adequadas.
   - Implementar um sistema de prompts dinâmicos que insira automaticamente o conteúdo relevante da **source** nas interações com a LLM, garantindo que a IA tenha acesso ao contexto atualizado.

4. **Persistência da Source**
   - Implementar uma solução de persistência para a **source** de acordo com o caso de uso, seja utilizando um banco de dados, armazenamento local ou outra opção adequada.
   - Garantir que as operações de leitura e escrita da **source** sejam eficientes e fáceis de escalar conforme o volume de dados aumenta, mantendo a simplicidade no design e na implementação.

5. **Processamento de Mensagens**
   - Desenvolver um sistema para processar as mensagens que o usuário envia à LLM, garantindo que a comunicação flua de forma natural e eficaz.
   - As mensagens (prompts) enviadas pelo usuário deverão ser de linguagem não técnica, descrevendo aspectos do seu negócio. A LLM deve ser capaz de interpretar essas mensagens e atualizar automaticamente a **source** de maneira clara e objetiva, refletindo as mudanças com precisão e concisão nas interações.

## Diferenciais

1. **Consultas e Insights**
   - Implementar funcionalidade que permita ao usuário formular perguntas em linguagem natural sobre os dados contidos na source, com a IA fornecendo respostas claras e objetivas. As interações devem ser dinâmicas e naturais, facilitando a exploração das informações e auxiliando o usuário na tomada de decisões informadas.
   - As respostas devem ser rápidas e úteis, garantindo que o usuário compreenda facilmente as informações relevantes para o seu negócio.
1. **Visualizações de Dados**
   - Implementar gráficos ou outras representações visuais que possam ser apresentadas diretamente no fluxo do chat, de acordo com as solicitações do usuário. Essas visualizações devem ser geradas dinamicamente com base nos dados contidos na **source**, refletindo as informações pertinentes durante a conversa.
1. **Otimização de Performance**
   - Implementar estratégias para lidar eficientemente com **"sources"** maiores, mantendo sempre a precisão nos dados.

## Dados de Exemplo

Abaixo está um exemplo de estrutura JSON que pode ser construída em colaboração com o usuário com base nas mensagens que ele envia. Este JSON representa informações relevantes que podem ser gerenciadas pela aplicação:

```json
{
  "fazenda": {
    "nome": "Fazenda Boa Esperança",
    "tamanho": 500,
    "unidade": "hectares"
  },
  "safras": [
    {
      "ano": 2023,
      "cultura": "Soja",
      "area_plantada": 300,
      "producao_total": 900,
      "unidade_producao": "toneladas"
    }
  ],
  "custos_operacionais": {
    "insumos": 500000,
    "mao_de_obra": 200000,
    "equipamentos": 300000,
    "moeda": "BRL"
  }
}
```

## Critérios de Avaliação

1. **Funcionalidade**: Cumprimento dos requisitos mínimos.
2. **Qualidade do Código**: Organização, legibilidade e uso adequado de TypeScript.
3. **Arquitetura**: Uso eficiente de Next.js, tRPC e Langchain.
4. **UX/UI**: Usabilidade e design da interface.
5. **Segurança**: Implementação de práticas básicas de segurança.
6. **Documentação**: Clareza das instruções de instalação e uso.

## Entrega do Projeto

- O projeto deve ser disponibilizado em um repositório Git público (como GitHub ou GitLab) e acompanhado de instruções claras para instalação e execução.
- O candidato tem a liberdade de definir as escolhas arquitetônicas, assim como o uso de testes, linters e documentação do projeto.
- É permitido o uso de tecnologias e conceitos diversos, desde que estes sejam adequadamente fundamentados e atendam ao caso de uso proposto, abordando as necessidades do usuário final.
