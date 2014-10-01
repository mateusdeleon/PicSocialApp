PicSocialApp
============

# Projeto e organização do repositório

## Utilização da arquitetura MVC e o diretório "/app"

Esse projeto utiliza a arquitetura de software MVC como forma de separar os dados relativos às interações e seus
layous. Dessa forma, há uma segurança maior em realizar mudanças no layout sem interferir no comportamento do programa. 
A pasta **/app** guarda os diretórios *controllers*, *models* e *views*:

* models: armazenará todos os objetos e dados do aplicativo. Esses objetos e dados só irão se comunicar com o restante do
aplicativo se sofrer alguma mudança.
* views: interface de interação com o usuário. Aqui ficam os arquivos de layout do aplicativo.
* controllers: faz a comunicação e toda a lógica entre as "camadas" *view* e *model*.

Leia um pouco mais sobre essa arquitetura no seguinte link:
[MVC Pattern Overview](https://developer.chrome.com/apps/app_frameworks#mvc)

### Diretório **/dist**

O diretório **/dist** foi colocado no arquivo .gitignore, pois trata-se apenas de uma "pasta-output" que representa a junção
das pastas **/app** e **/www**.

## Fluxo do repositório

O fluxo do repositório estará orientado ao conceito de "feature-branches", onde o usuário cria um branch cópia do Master
(por ex: fix-layoutCorrection) para realizar suas implementações. Feitas as implementações, o usuário deve enviar um 
*pull request* em direção ao branco upstream-master. É importante ressaltar que o branch master do usuário só deverá 
ser atualizado pelo branch upstream-master.

**Jamais fazer push em direção ao remote upstream!**

Mais informações sobre feature-branches: [Feature Branch WorkFlow]
(https://www.atlassian.com/git/tutorials/comparing-workflows/feature-branch-workflow)