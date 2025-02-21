# Versionamento do Power BI com Git
O objetivo deste repositório é exemplificar o versionamento do Power BI com o git.


## Pré-requisitos
* Git instalado

* Configurar o git com o seu user e email

* Power BI Desktop instalado

* Salvar o arquivo Power BI com a extensão ```.pbip```

Exemplo do arquivo:

![image](assets/pbip.png)


## Comandos git
Inicializar o git
```
git init
```

Verificar o status do projeto
```
git status
```

Adicionar alterações a ser versionada no track
```
git add <file>
```

Remover arquivo do track
```
git rm --cached <file>
```

Desfazer alterações
```
git restore <file>
```

Faça um commit inicial
```
git commit -m "Initial commit"
```

Verificar todos os commits (esse comando é útil para verificar todas as versões do teu projeto)
```
git log
```

Resultado esperado:

![image](assets/git-log.png)


## Como voltar para um commit específico?
```
git checkout <hash do commit>
```

⚠️ Esse comando vai te levar o momento que a commit escolhido foi feito. Cabe ressaltar que ele apenas te direciona para essa branch, mas não apaga tudo que foi feito depois. Esse comando serve apenas para você avaliar como era o projeto naquele momento. 

## O que são branches?
São separações do seu projeto em ramificações.

## Criar uma branch nova
```
git branch feature/add_new_feature
```

## Como ver todas as branches?
```
git branch
```

Resultado esperado:
![image](assets/git-branch.png)


Depois de fazer checkout na branch nova e adicionar a modificação, o seu código precisa ser integrado na branch principal. Para isso você precisará fazer o commit da alteração na branch paralela, fazer checkout na principal e depois puxar alterações para a branch principal com o comando:
```
git merge 
```

⚠️ Cabe ressaltar que o mais comum é que essa passagem seja feita via ```Pull Request (Github)``` ou ```Merge Request (Gitlab)```. Caso não sabia, mas esse processo é implementado para que uma aprovação seja feita antes da mesclagem de códigos.

## ❌ Conflitos no git
Se o mesmo arquivo for alterado em branchs diferentes, o git vai identificar um conflito na hora do merge e será necessário que você escolha qual a versão do código que vale.

## Como deletar um  branch?
```
git branch -d <branch-name>
```

## Como voltar para uma versão de forma definitiva?
```
git reset --hard <hash do commit>
```

⚠️ Atenção que esse comando apaga tudo que foi feito depois do commit e de forma definitiva.

## Sincronização com o Github (ou o seu hub de códigos)
Será necessário primeiro criar um repositório no seu hub e depois criar um vínculo com o repositório local.

## Como vincular um repositório local com o remoto?
```
git remote add origin https://github.com/wlcamargo/pbi-devops.git
```

## Como enviar o código para o hub?
No primeiro push:
```
git push --set-upstream origin main
```

A partir da segunda vez, basta realizar o comando:
```
git push
```

## 📚 Referências
https://learn.microsoft.com/pt-pt/power-bi/developer/projects/projects-git

## 🧑🏼‍🚀 Developer
| Desenvolvedor      | LinkedIn                                   | Email                        | Portfólio                              |
|--------------------|--------------------------------------------|------------------------------|----------------------------------------|
| Wallace Camargo    | [LinkedIn](https://www.linkedin.com/in/wallace-camargo-35b615171/) | wallacecpdg@gmail.com        | [Portfólio](https://wlcamargo.github.io/)   |
