# PortalInvoiCyArgentina
Portal de documentação técnica de integração com o InvoiCy Argentina utilizando o framework MKDOCS.


Como atualizar os artigos:
- Clone o repositório na sua máquina.
- instale o Python +3.10.
- Instale o Poetry via terminal
    ```shell
    pip install poetry
    ```
- Rode o comando abaixo para carregar as dependências, como MKDOCS.
    ```shell
    poetry install
    ```
- Todos os artigos devem ser cridos em arquivos .md dentro do diretório "docs".
- Itens no menu devem ser incluídos no index.md.

Como testar aplicação local:
- rode no terminal o comando abaixo:
    ```shell
    mkdocs serve
    ```
- Vai ser disponibilizado localmente um serviço em 127.0.0.1:8000/PortalInvoiCyArgentina/
- Será criado um diretório "site" com os arquivos estáticos. Este diretorio está para ser ignorado no .gitignore, pois não é necessário depois.

Como subir para produção:
- Comite todas as alterações e atualize o repositório remoto, pois essa é a versão original para qualquer pessoa alterar.
    ```shell
    git add <arquivos>
    git commit -m "descrição do commit"
    git push
    ```

- Execute o comando para gerar uma branch "gh-pages":
    ```shell
    mkdocs gh-deploy
    ```
- Automaticamente o mkdocs irá subir essa branch para o repositório do github e habilitar a página.
- Em instantes estará atualizado em https://migrate-company.github.io/PortalInvoiCyArgentina/preguntasmasfrecuentes/
