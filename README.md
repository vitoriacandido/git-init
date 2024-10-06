# Configurações básicas do Git

## Instalação
- [GitForWindows](https://gitforwindows.org/)

## Config
Após a instalação é necessário realizar a sua primeira configuração, neste caso, identificando o nome e o e-mail de quem estará atrelado as alterações.
```
git config --global user.name "Nome Sobrenome"
git config --global user.email "seu_email@example.com"
```

## Init
```
git init
git add . 
git commit -m "Comentário a ser adicionado"
git push
```

## Atualizar o repositório local
Ao utilizar diferentes locais para trabalho se faz necessário sua atualização sempre que for dar início, pois, pode ser que as alterações realizadas não tenho sido baixadas na máquina local.
```
git pull
```

## Copiar um repositório existente
```
git clone <link-repositorio>
```

# Git Bash no menu de contexto do Windows

1. Abra o bloco de notas (notepad) e salva o documento com o nome `OpenGitBash.reg`

![image](https://github.com/user-attachments/assets/9c6e9b17-cd6e-44b9-9050-ae3f5e7fb520)

2. Copia e cola o conteúdo abaixo para dentro do **bloco de notas**

```
Windows Registry Editor Version 5.00
; Open files
; Default Git-Bash Location C:\Program Files\Git\git-bash.exe

[HKEY_CLASSES_ROOT\*\shell\Open Git Bash]
@="Open Git Bash"
"Icon"="C:\\Program Files\\Git\\git-bash.exe"

[HKEY_CLASSES_ROOT\*\shell\Open Git Bash\command]
@="\"C:\\Program Files\\Git\\git-bash.exe\" \"--cd=%1\""

; This will make it appear when you right click ON a folder
; The "Icon" line can be removed if you don't want the icon to appear

[HKEY_CLASSES_ROOT\Directory\shell\bash]
@="Open Git Bash"
"Icon"="C:\\Program Files\\Git\\git-bash.exe"


[HKEY_CLASSES_ROOT\Directory\shell\bash\command]
@="\"C:\\Program Files\\Git\\git-bash.exe\" \"--cd=%1\""

; This will make it appear when you right click INSIDE a folder
; The "Icon" line can be removed if you don't want the icon to appear

[HKEY_CLASSES_ROOT\Directory\Background\shell\bash]
@="Open Git Bash"
"Icon"="C:\\Program Files\\Git\\git-bash.exe"

[HKEY_CLASSES_ROOT\Directory\Background\shell\bash\command]
@="\"C:\\Program Files\\Git\\git-bash.exe\" \"--cd=%v.\""
```

3. Execute o arquivo clicando duas vezes
4. Irá pedir que autorize no modo administrador, clique em `Sim`
   
![image](https://github.com/user-attachments/assets/e2dbc61c-9377-41fb-a398-009bcd5bc8d2)

6. Então, a instalação será realizada no registro.
   
![image](https://github.com/user-attachments/assets/7d314577-26bb-44ea-878f-2d315ebb47c6)

8. Agora, só abrir alguma pasta e clicar com o botão direito. Irá notar que irá aparecer a opção `Open Git Bash`. 
Nota que estou utilizando o Windows 11.

<div align="left">
  <img src="https://github.com/user-attachments/assets/d0c36ce4-09f5-4059-a5e7-8a385440f776" width="50%" />
</div>


