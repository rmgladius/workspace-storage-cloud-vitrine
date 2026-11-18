<p align="center">
  <img src="docs/imagens/capa.png" alt="Workspace Storage Cloud: todas as suas ferramentas, em um lugar só." width="100%">
</p>

<p align="center">
  <a href="https://workspacestoragecloud.com.br"><b>Conhecer a plataforma</b></a>
  &nbsp;·&nbsp; no navegador do computador ou do celular &nbsp;·&nbsp; licença anual
</p>

A Workspace Storage Cloud é uma plataforma de aplicativos para engenharia, topografia e BIM. Cada
cliente cria a conta, contrata a licença e trabalha num ambiente só dele, com os aplicativos lado a
lado no mesmo painel: cadastro e perfil de sondagens, cadastro topográfico em campo, configuração da
exportação IFC do Civil 3D e um editor de modelos IFC em 3D.

<p align="center">
  <img src="docs/imagens/demo.webp" alt="O Editor IFC 3D com uma casa de exemplo: uma parede é selecionada e as propriedades dela aparecem ao lado, o telhado entra na seleção com Ctrl, o modelo gira e passa pelos estilos Linha oculta e Aramado." width="100%">
</p>

## Editor IFC 3D

<p align="center">
  <img src="docs/imagens/editor-3d.png" alt="Editor IFC 3D: a estrutura do projeto em árvore e as propriedades da parede selecionada à esquerda, e o modelo da casa em 3D à direita, com a parede em destaque." width="100%">
</p>

Abre modelos IFC (IFC2X3, IFC4 e IFC4X3) de qualquer programa de BIM direto no navegador. A
estrutura do projeto aparece em árvore, e cada objeto mostra atributos, propriedades e tipo, todos
editáveis: dá para trocar a classe, mudar valores de vários objetos de uma vez e exportar um IFC
novo. O modelo é lido no próprio navegador e só vai para a conta quando a pessoa salva.

## Cadastro de Sondagens

<p align="center">
  <img src="docs/imagens/sondagens.png" alt="Cadastro de Sondagens: seis furos sobre a imagem de satélite de um terreno, quatro executados e dois programados, com as opções de importar pontos e exportar para Google Earth e Civil 3D." width="100%">
</p>

Os furos entram por planilha, digitados ou clicando no satélite. O aplicativo converte as
coordenadas UTM, separa o que já foi executado do que está programado e exporta para Google Earth
(KMZ e KML), planilha e Civil 3D. Um código de acesso deixa outras pessoas trabalharem no mesmo
projeto.

## Perfil de Sondagem

<p align="center">
  <img src="docs/imagens/perfil.png" alt="Folha do perfil individual de sondagem SP-01: camadas de aterro, argila siltosa, areia siltosa, silte arenoso e rocha alterada, com os golpes do SPT, o índice N em gráfico e o nível d'água." width="70%">
</p>

O boletim do furo, como pede a NBR 6484: camadas com a hachura de cada solo, golpes do SPT, índice N
em gráfico, nível d'água e motivo da paralisação. A folha A4 é redesenhada a cada tecla e sai pronta
para imprimir ou salvar em PDF, com a logo e as assinaturas da empresa. Ligado a um furo do Cadastro
de Sondagens, o boletim já vem com coordenada e cota.

## Cadastro Topográfico

<p align="center">
  <img src="docs/imagens/topografico.png" alt="Cadastro Topográfico: postes, árvores, poços de visita, hidrante e abrigo de ônibus marcados com símbolos técnicos ao longo de duas ruas, e a lista dos pontos abaixo do mapa." width="100%">
</p>

Postes, árvores, poços de visita, hidrantes, placas e outros elementos de via, cada um com o seu
símbolo técnico. No campo, o celular cadastra o ponto onde a pessoa está, pelo GPS e com foto. No
escritório, basta clicar no satélite. Sai em KMZ, KML, planilha e Civil 3D.

## Configurador IFC

<p align="center">
  <img src="docs/imagens/configurador.png" alt="Configurador IFC: as seções do mapeamento do Civil 3D à esquerda e, à direita, as camadas com a classe IFC de cada uma e a chave que decide se ela é exportada." width="100%">
</p>

O Civil 3D exporta para IFC a partir de dois arquivos JSON, mas não tem tela para editá-los. Aqui
eles abrem em português e separados por assunto: a classe IFC de cada camada, estilo e código, o
que entra ou fica de fora e as opções da exportação. O arquivo volta no mesmo formato em que entrou.

## O painel

<p align="center">
  <img src="docs/imagens/painel.png" alt="Catálogo de aplicativos do painel, com busca, filtros e os cinco aplicativos em cartões." width="100%">
</p>

Os aplicativos ficam num catálogo com busca e filtros, e os mais usados vão para o acesso rápido. Na
conta estão o perfil, a verificação em duas etapas, a licença, os contratos, a exportação dos dados
pessoais e o suporte por chamados. A equipe cuida de clientes, preços, cupons, contratos, e-mails e
newsletter numa área administrativa própria.

## O site

<p align="center">
  <img src="docs/imagens/site.png" alt="Página inicial do site: Todas as suas ferramentas. Em um lugar só., com os botões Criar conta e Conhecer a plataforma e uma prévia do painel." width="100%">
</p>

Páginas de aplicativos, planos, sobre e contato, nos temas claro e escuro. No cadastro, o CNPJ é
conferido na Receita na hora, e dá para entrar com a conta Google.

## No celular

<p align="center">
  <img src="docs/imagens/celular.png" alt="Três telas no celular: a página inicial do site, o catálogo de aplicativos e o Cadastro Topográfico com o mapa e o botão Cadastrar onde estou." width="100%">
</p>

Tudo funciona no celular, do site ao painel. No Cadastro Topográfico, é por ele que o técnico
registra os pontos em campo.

## Por dentro

A plataforma foi feita em Laravel com Inertia, React e TypeScript, com Tailwind CSS e componentes
shadcn/ui. Todos os clientes ficam num banco MariaDB só, e o isolamento é feito pela aplicação: toda
tabela de cliente leva o identificador do ambiente, e uma guarda recusa a consulta que chegue a ela
sem esse filtro. Assim tudo roda numa hospedagem compartilhada comum.

A licença anual é paga pelo Mercado Pago. A conta tem verificação em duas etapas, limite de sessões
simultâneas e trilha de auditoria, e cada página tem a sua política de segurança de conteúdo (CSP).
O 3D usa three.js e web-ifc, e os mapas, Leaflet. São mais de 700 testes automatizados.

Laravel · PHP 8.4 · Inertia · React · TypeScript · Tailwind CSS · MariaDB · three.js · web-ifc ·
Leaflet · Mercado Pago · PHPUnit

O código fica num repositório privado. Este repositório é a vitrine do projeto. As telas usam dados
de demonstração, e a casa do Editor IFC 3D é o modelo de exemplo AC20-FZK-Haus, do Instituto de
Tecnologia de Karlsruhe (KIT).

---

Feito por [Rodrigo Dias](https://github.com/rmgladius).
