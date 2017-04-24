---
title: "Git uma ideia - Thoughts #1"
excerpt: "Um breve texto mostrando a importância de ferramentas de versionamento de código, em específico o git."
category: "Thoughts"
header:
    teaser: "/assets/images/github-octocat_yes-we-code.jpg"
---

**_Welcome stranger_**, se você já desenvolve há algum tempo já deve ter
sentido a necessidade de se salvar um código em um espaço que não seja o
da sua máquina, ou indo mais longe, provalmente já deve ter ouvido falar
sobre ferramentas de versionamento de código, e mais especificamente falar
em _git_.

Muitas pessoas quando começam a aprender a programar para salvar o trabalho
já feito apelam para o armazenamento interno de sua máquina, outras já apelam
para ferramentas de armazenamento de arquivos, como Dropbox, One Drive entre
outros.

Sinceramente não há nada de errado nisso, você é livre para escolher a
ferramenta que mais lhe atende, mas aqui vou lhe mostrar o por que você
deveria começar a usar o git.

![Octocat Bombado](/assets/images/steroidtocat.png "Octocat Bombado"){: .aligncenter}

Primeiramente não se deixe assustar pelo gato acima, aquele é o Octocat, o
mascote do **GitHub**, que entrarei em detalhes mais a frente, vamos por partes.

O que é? E como funciona?
-------------------------

Como já dito o _git_ é uma ferramenta de versionamento, com ela é possível manter a história
do seu código, ver as últimas alterações, e se for o caso, reverter para versões antigas
do código. Ele também possibilita manter uma versão do seu código em servidores remotos, possibilitando
o fácil compartilhamento e a portabilidade do código. As suas aplicações individualmente são separadas
no que o _git_ define como um repositório, o repositório nada mais é onde seu código fonte fica salvo.

Servidores Remotos? Como assim?
-------------------------------

Sim, você manter seu código na nuvem, podendo baixar em qualquer máquina e continuar seu trabalho, sem se
preocupar em fazer backups e afins, o próprio versionamento na nuvem serve como um backup para você,
mas é claro o ambiente ainda será um problema para outra hora (pyenv <3).

Mas e a privacidade do meu código como fica?
--------------------------------------------

Existem dois servidores remotos que eu recomendo, o já mencionado [**GitHub**](https://github.com)
e o [**Bitbucket**](https://bitbucket.com), o serviço prestado pelos dois é basicamente o mesmo e de
graça, com apenas um diferencial, a privacidade do código em si, no **GitHub** por _default_ todos os
repositórios são públicos, e como isso já sugere, qualquer um com acesso ao site poderá ver seu código
(inclusive este site está sendo hospedado usando o **GitHub**, e todo código dele pode ser visto lá),
caso você queira ter repositórios privados o site oferece planos pago para isso.

Já no **Bitbucket** todos os seus repositórios são privados, a única limitação acontece quanto a organizações
(grupo de programadores que compartilham repositórios em resumo), sendo neste caso a quantidade de membros
na organização, que no máximo é de 5 integrantes, ele também oferece planos pagos para esse quesito.

Se você quiser ir um pouco mais longe, você pode criar o seu próprio servidor remoto, um exemplo seria o
**GitLab** que dispoem de ferramentas para isso.

Hmmm... A ideia parece legal... mas tem algo mais?
--------------------------------------------------

Se você ainda não se convenceu, aqui vai uma dica importante: muitas empresas contratam pelo seu perfil no
**GitHub**, você já deve ter chegado a conclusão que pelos projetos no site serem abertos naturalmente o site é
um aglomerado de projetos _open source_, muitas das pessoas que contribuem em projetos _open source_ conseguem
seus trabalhos por intermédio do **GitHub**.

Concluindo
----------

Espero que eu tenha ao menos lhe deixado com a pulga atrás da orelha pra pelo menos ter curiosidade
de começar a estudar a ferramente. Aqui também ressalvo que existem outras empresas que utilizam o _git_
para versionamento de projetos, mas não só de códigos fontes, e sim arquivos de projetos de outros tipos
de softwares, como por exemplo design de placas de circuitos integrados, quem sabe não aparece por aqui
um tutorial básico de como usar o _git_? Bom, me despeço aqui, espero que tenham gostado da leitura,
e desejo a vocês um **_happy coding_**.




