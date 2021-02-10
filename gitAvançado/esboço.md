# Commando git que quando você precisar você vai agradecer
Uma breve spreadsheet de alguns commando mais avançados de git que ficam de curiosidade e em algum momento podem ser utils

## git clone <url> <dir> 
Sim! você pode passar o nome do diretorio direto no git clone

## git add -i 
Sabe aquela barra de git do vscode? é tipo isso. Ele mostra um pequeno menu
te permitindo ver as diferenças entre arquivos, selecionar ele ou descelecionar.
Mas não é lá a melhor UX que vc vai ter

## git add -p <file> 
Te permite commitar apenas parte das alterações em um arquivo

## git commit -v
Abre o seu editor de texto e mostra todas as alterações no arquivo, bem util pra quando você não lembra direito no que mexeu

## git commit -a
Adiciona os arquivos [rastreados](https://git-scm.com/book/pt-br/v2/Fundamentos-de-Git-Gravando-Altera%C3%A7%C3%B5es-em-Seu-Reposit%C3%B3rio#_gravando_altera%C3%A7%C3%B5es_em_seu_reposit%C3%B3rio)
(Arquivos que já foram algumas vez modificados) e commita

## git commit --amend
Um `git reset --soft HEAD~ && git commit`, permite você incluir alterações no ultimo commit.
Cuidado isso vai reescrever seu historico ( e se vc já deu um push, vai ter que dar um push --force)

## git push --force
Esse você provavelmente conhece, permite a você forçar o repositorio remoto (leia-se github/gitlab/bitbucket)
a aceitar o seu repositorio, sobrescrevento tudo que tem lá (alterações de outras pessoas por exemplo). Use com sabedoria

## \~ e ^
Permite a você referencia commits pais com maior facilidade, a diferença entre 
eles é de onde começam a contar, HEAD\~1 == HEAD^0, o ^ começa a partir do pai do atual
e o \~ a partir do atual. Por motivos que eu já não sei se vc só usar HEAD\~ = HEAD^ = HEAD~1

## git stach
Permite a você a commitar em um universo paralelo, e depois recuperar esse commit. Util quando vc fez algo pela metade e não quer commitar.
Minha explicação ficou besta pq a [documentação](https://git-scm.com/book/pt-br/v2/Git-Tools-Stashing-and-Cleaning) é muito boa.

## [git rebase -i](https://git-scm.com/book/pt-br/v2/Git-Tools-Rewriting-Historyhttps://git-scm.com/book/pt-br/v2/Git-Tools-Rewriting-History)
Perfeito pra trocar a ordem entre commits, reescrever mensagens, mesclar commits e outras coisas interessantes

## [git filter-branch](https://git-scm.com/book/pt-br/v2/Git-Tools-Rewriting-History)
Esse aqui permite a você reescrever a historia por meio de script,
util para quando uma grande quantidade de commits para se tirar um arquivos de senhar por exemplo

## git bisec
Roda uma busca binaria no seu historico. Util apara caçar bugs. Você define quando
estava funcionando (good) e quando parou (bad) e a partir dai o git vai te jogando
para momentos, apos testar vc avisa se estava funcionando ou não, e após alguns
passos ele identifica onde houve um problema.
Ele pode testar automaticamente com o `git bisect run`



