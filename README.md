# Linux Ubuntu Docs
Documentação pessoal sobre assuntos relacionados a distribuição Ubuntu e outras coisas voltadas para o ambinete Linux


## Como criar uma atalho nos aplicativos no ubuntu
### Exemplo com o Postman

1. Fazer download do postman https://www.postman.com/downloads/
2. Extrair o postman ```tar -xzf Postman-linux-x64-<versao>.tar.gz ``` 
3. Mover para a pasta /opt/Postman  ```sudo rm -rf Postman /opt/Postman ```
4. Criar um link simbolico ```sudo ln -s /opt/Postman/Postman /usr/bin/postman``` 
5. Criar arquivo do desktop
``` 
cat > ~/.local/share/applications/postman.desktop <<EOL
[Desktop Entry]
Encoding=UTF-8
Name=Postman
Exec=postman
# Before v6.1.2
# Icon=/opt/Postman/resources/app/assets/icon.png
Icon=/opt/Postman/app/resources/app/assets/icon.png 
Terminal=false
Type=Application
Categories=Development;
EOL
``` 
6. Remover o download ```rm Postman-<versao>.tar.gz```
