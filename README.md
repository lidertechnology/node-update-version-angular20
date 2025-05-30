# node-update-version-angular20

Pasos para Configurar Node.js (con NVM) en Entornos de Nube

1. Elimina NPM_CONFIG_PREFIX:

En la terminal: 

    unset NPM_CONFIG_PREFIX
  
Edita tu archivo de configuración (nano ~/.bashrc o nano ~/.zshrc). Busca y comenta o elimina cualquier línea que contenga export NPM_CONFIG_PREFIX o NPM_CONFIG_PREFIX=. Guarda el archivo.

2. Instala NVM (Node Version Manager):

Bash

    curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash

3. Carga NVM en la sesión actual:

Bash

    export NVM_DIR="$HOME/.nvm"
    [ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"
    [ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"

4. Instala la versión de Node.js requerida:

Bash

    nvm install 20.19.0
    # O para la última LTS:
    # nvm install --lts
    Establece la versión como predeterminada:

Bash

    nvm alias default 20.19.0
    # O si usaste --lts, la versión que NVM te indique
    Instala Angular CLI (u otras herramientas globales):

Bash

    npm install -g @angular/cli

Reinicia la sesión y verifica:

Cierra tu pestaña de Cloud Shell (o el entorno de nube IDE).
Vuelve a abrirla.
Verifica: 


    node -v, npm -v, ng version.
    
Siguiendo estos pasos, tus configuraciones de Node.js y Angular CLI persistirán en futuras sesiones.
