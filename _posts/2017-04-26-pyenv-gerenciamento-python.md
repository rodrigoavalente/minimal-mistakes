---
title: "Pyenv, Gerenciamento do Python - Thoughts #2"
excerpt: "Uma breve conversa mostrando como gerenciar seu ambiente
de desenvolvimento utilizando pyenv."
category: "Thoughts"
header:
    teaser: "/assets/images/pythonlogo.jpg"
---

{% include toc icon="list-alt" title="Navegação" %}

**_Welcome stranger_**, que atire a primeira pedra quem nunca teve dores
de cabeça com versões de uma ferramenta de desenvolvimento? Aposto que você
já passou por problemas com a versão do seu interpretador do _PHP_, ou com a
versão da _JDK_ instalada, basta uma atualização e todo o seu código quebra,
daí numa tentativa de desespero você tenta desinstalar as novas versões e
reinstalar as velhas, e quando se depara já está preso em uma bela bola de nova e você perde horas tentando corrigir o seu ambiente enquanto poderia estar desenvolvendo :(

Bom, felizmente nem tudo precisa ser assim, diversas linguagens de programação
atualmente dispoem de ferramentas que lhe auxiliam nisso, nesse artigo especificamente vou tratar do _pyenv_, um gerenciador de instalações do _python_, mas como dizia Jack Estripador, vamos por partes.

O que é o _pyenv_?
------------------

Como dito anteriormento, ele é basicamente um gerenciador de instalações do _python_, em projetos com a linguagem é bem comum se utilizar apenas uma versão, e para evitar que o código quebre o _pyenv_ utiliza de _shell scripts_(_scripts_ que rodam no terminal do linux) para alterar a versão utilizada no projeto, somado ao fato dele utilizar uma ferramenta nativa da linguagem, os _virtualenvs_, que tem o mesmo próposito, contudo o _pyenv_ organiza melhor as instalações das versões em um único diretório e possibilita a troca automática do ambiente por projeto.

Que maravilha, onde posso encontrar?
------------------------------------

O _pyenv_ é um projeto de código livre, pode ser encontra em seu repositório no **GitHub** [aqui](https://github.com/pyenv/pyenv).
Caso não saiba o que é o **GitHub** ou até mesmo _git_, eu faço uma explicação sobre o assunto nesse outro [post](/thoughts/git-uma-ideia).

Utilizando o _pyenv_
--------------------

Nessa seção a parte irei exemplificar como instalar e utilizar a ferramente, vocês verão que é muito simples e não causa nenhum transtorno.

### Instalando o _pyenv_

Para aqueles que usam MAC OSX o _pyenv_ já está disponível no _homebrew_, bastando o utilizar para obter o software. Já para aqueles que utilizam o sistemas linux, existe um projeto no **GitHub** chamado de [_pyenv installer_](https://github.com/pyenv/pyenv-installer), e é muito simples, não é necessário baixar o repositório diretamente, em um terminal execute:

```
curl -L https://raw.githubusercontent.com/pyenv/pyenv-installer/master/bin/pyenv-installer | bash
```
Para executar o comando acima será necessário utilizar o _cUrl_, praticamente toda distribuição linux já vem com ele instalado, ele irá baixar o _script_ do instalador o comando após o pipe diz que o arquivo deve ser interpretado pelo _bash_. Terminado o comando você já terá o pyen em sua máquima bastando executar a atulização do mesmo com o comando:

```
pyenv update
```

Nota: Oficialmente não existe uma versão do _pyenv_ para o Windows, logo não é possível instala-lo no sistema, e também não irei me aprofundar nisso, pessoalmente não acho que Windows seja uma boa plataforma para programação, tem suas vantagens, porém eu enxergo mais desvantagens em utiliza-lo.

### Baixando versões do _python_

Com o _pyenv_ instalado é possível realizar a instalação de outras versões do _python_, para listar as versões disponíveis remotamente você pode utlizar o seguinte comando:

```
pyenv install --list
# Exemplo de saída do comando
  2.1.3
  2.2.3
  2.3.7
  2.4.0
  2.4.1
  2.4.2
  2.4.3
  2.4.4
  2.4.5
  2.4.6
```

Feito isso basta escolher uma das versões, digamos que a versão escolhida foi a `2.4.6`, logo:

```
pyenv install 2.46
```

### Alterando as versões

Por padrão o _pyenv_ utiliza a versão do python já disponível em sua máquina, para alternar para uma versão já instalada utilize:

```
# Alternando a versão em um terminal local
pyenv shell <versao>

# Ou, alternando a versão globalmente
pyenv global <versao>
```

### Criando um ambiente virtual

Aqui que está a mágica de se utilizar o _pyenv_, nos ambientes virtuais podemos aglomerar todas as depêndencias do nosso projeto, sendo estas instaladas por uma versão do python, sem prejudicar todo o ambiente, para isso basta fazer:

```
pyenv virtualenv <versao> <nome_do_ambiente>
```

Feito isso o _pyenv_ criará um ambiente virtual e o ativará automaticamente, esse ambiente é totalmente isolado da sua instalação padrão do _python_, se ocorrer algum problema basta removê-lo. Para que o ambiente seja ativado automaticamente quando você acessar o diretório do seu projeto, basta que, dentro do diretório do projeto, você execute:

```
pyenv local <nome_do_ambiente>
```

O _pyenv_ criará um arquivo `.python-version` que ele utilizará para ativar o ambiente.

### Desinstalando uma versão do _python_ ou um ambiente virtual

Bom, já foi visto como instalar uma versão do python, basicamente é fácil deduzir que fazer a desinstalação segue um caminho parecido:

```
pyenv uninstall <versao>
```

Simples assim. Para remover um ambiente virtual é um pouco mais complexo:

```
pyenv virtualenv-delete <nome_do_ambiente>
```

Concluindo
----------

Espero que tenham gostado da leitura, eu utilizo o _pyenv_ em basicamente todos os meus projetos _python_ quando eu o descobri, seu gerenciamente me facilitou muito nos trabalhos e agilizou a montagem do ambiente para desenvolvimento. Irei me despedir aqui, lhes desejo um ótimo dia e um **_happy coding_**.


