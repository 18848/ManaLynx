# ManaLynx
## Siglas
- RNF -> Requisito Não-Funcional
- UX -> User Experience

## Requisitos Não-Funcionais
Os requisitos não-funcionais (RNF), são essenciais para a elaboração de um projeto, uma vez que tendem a dar resposta a pontos cruciais, tais como segurança, escabilidade, manutenção, entre outros.

Os RNF definidos para este projeto são os seguintes:

- Escabilidade, todo o projeto deve ser desenhado com o intuito de ser melhorado e ser capaz de suportar novas features;
- Usabilidade, queremos que a plataforma seja user-friendly, essa parte deverá ser focada no front-end, onde o UX é o ponto fulcral;
- Segurança, este é talvez o aspeto mais importante e aquele onde deve ser depositada mais atenção e mais cuidado. Pelo tema do trabalho, são tratados dados sensíveis. Os dados serão encriptados pelo back-end e toda a comunicação dos dados deve ser feita de forma encriptada.
- Integridade de Dados, devemo-nos responsabilizar por manter, de forma segura, os dados relativos aos clientes, assegurando que dado algum seja perdido ou corrompidos.
- Disponibilidade, como o projeto pretende retratar uma plataforma online, é necessário assegurar que o servidor consegue assegurar um certo número de utilizadores e que está ativo em todo o momento.
- Updates, qualquer update deve ter em conta a disponibilidade dos serviços, sendo que os updates devem surgir com pouca regularidade, mas com bastante eficiência (evita updates pequenos com muita regularidade).
- Interoperabilidade, com o mesmo software, é suposto que três classes de utilizadores ( , ,) consigam utilizar o mesmo software, com o respetivo acesso a que tem permissão.
- Regulação, uma vez que o negócio trabalha com dados sensíveis, deverá ser elaborado um termo de utilização que assegure pontos importantes de utilização da aplicação.


## Webgrafia
Para fazer as citações:
https://www.citationmachine.net/apa

[1] A. Saggu, “Non-functional requirements in software engineering,” GeeksforGeeks, 04-Jun-2020. [Online]. Available:
https://www.geeksforgeeks.org/non-functional-requirements-in-software-engineering/?ref=lbp. [Accessed: 04-Mar-2022]. 

[2]  “Encrypting data,” Microsoft Docs. [Online]. Available:
https://docs.microsoft.com/en-us/dotnet/standard/security/encrypting-data. [Accessed: 04-Mar-2022]. 


Reliability
Regulatory
Maintainability
Serviceability
Manageability
Capacity
Environmental

Performance constraints – Reliability, security, response time, etc.
Operating constraints – These include physical constraints (size, weight), personnel availability, skill level considerations, system accessibility for maintenance, etc.
Interface constraints – These describe how the system is to interface with its environment, users, and other systems. For example, user interfaces and their qualities (e.g., user-friendliness).
Economic constraints – Immediate and/or long-term costs.
Lifecycle requirements – Quality of the design: These measured in terms such as maintainability, enhance ability, portability.



Dillinger is a cloud-enabled, mobile-ready, offline-storage compatible,
AngularJS-powered HTML5 Markdown editor.

- Type some Markdown on the left
- See HTML in the right
- ✨Magic ✨

## Features

- Import a HTML file and watch it magically convert to Markdown
- Drag and drop images (requires your Dropbox account be linked)
- Import and save files from GitHub, Dropbox, Google Drive and One Drive
- Drag and drop markdown and HTML files into Dillinger
- Export documents as Markdown, HTML and PDF

Markdown is a lightweight markup language based on the formatting conventions
that people naturally use in email.
As [John Gruber] writes on the [Markdown site][df1]

> The overriding design goal for Markdown's
> formatting syntax is to make it as readable
> as possible. The idea is that a
> Markdown-formatted document should be
> publishable as-is, as plain text, without
> looking like it's been marked up with tags
> or formatting instructions.

This text you see here is *actually- written in Markdown! To get a feel
for Markdown's syntax, type some text into the left window and
watch the results in the right.

## Tech

Dillinger uses a number of open source projects to work properly:

- [AngularJS] - HTML enhanced for web apps!
- [Ace Editor] - awesome web-based text editor
- [markdown-it] - Markdown parser done right. Fast and easy to extend.
- [Twitter Bootstrap] - great UI boilerplate for modern web apps
- [node.js] - evented I/O for the backend
- [Express] - fast node.js network app framework [@tjholowaychuk]
- [Gulp] - the streaming build system
- [Breakdance](https://breakdance.github.io/breakdance/) - HTML
to Markdown converter
- [jQuery] - duh

And of course Dillinger itself is open source with a [public repository][dill]
 on GitHub.

## Installation

Dillinger requires [Node.js](https://nodejs.org/) v10+ to run.

Install the dependencies and devDependencies and start the server.

```sh
cd dillinger
npm i
node app
```

For production environments...

```sh
npm install --production
NODE_ENV=production node app
```

## Plugins

Dillinger is currently extended with the following plugins.
Instructions on how to use them in your own application are linked below.

| Plugin | README |
| ------ | ------ |
| Dropbox | [plugins/dropbox/README.md][PlDb] |
| GitHub | [plugins/github/README.md][PlGh] |
| Google Drive | [plugins/googledrive/README.md][PlGd] |
| OneDrive | [plugins/onedrive/README.md][PlOd] |
| Medium | [plugins/medium/README.md][PlMe] |
| Google Analytics | [plugins/googleanalytics/README.md][PlGa] |

## Development

Want to contribute? Great!

Dillinger uses Gulp + Webpack for fast developing.
Make a change in your file and instantaneously see your updates!

Open your favorite Terminal and run these commands.

First Tab:

```sh
node app
```

Second Tab:

```sh
gulp watch
```

(optional) Third:

```sh
karma test
```

#### Building for source

For production release:

```sh
gulp build --prod
```

Generating pre-built zip archives for distribution:

```sh
gulp build dist --prod
```

## Docker

Dillinger is very easy to install and deploy in a Docker container.

By default, the Docker will expose port 8080, so change this within the
Dockerfile if necessary. When ready, simply use the Dockerfile to
build the image.

```sh
cd dillinger
docker build -t <youruser>/dillinger:${package.json.version} .
```

This will create the dillinger image and pull in the necessary dependencies.
Be sure to swap out `${package.json.version}` with the actual
version of Dillinger.

Once done, run the Docker image and map the port to whatever you wish on
your host. In this example, we simply map port 8000 of the host to
port 8080 of the Docker (or whatever port was exposed in the Dockerfile):

```sh
docker run -d -p 8000:8080 --restart=always --cap-add=SYS_ADMIN --name=dillinger <youruser>/dillinger:${package.json.version}
```

> Note: `--capt-add=SYS-ADMIN` is required for PDF rendering.

Verify the deployment by navigating to your server address in
your preferred browser.

```sh
127.0.0.1:8000
```

## License

MIT

**Free Software, Hell Yeah!**

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)

   [dill]: <https://github.com/joemccann/dillinger>
   [git-repo-url]: <https://github.com/joemccann/dillinger.git>
   [john gruber]: <http://daringfireball.net>
   [df1]: <http://daringfireball.net/projects/markdown/>
   [markdown-it]: <https://github.com/markdown-it/markdown-it>
   [Ace Editor]: <http://ace.ajax.org>
   [node.js]: <http://nodejs.org>
   [Twitter Bootstrap]: <http://twitter.github.com/bootstrap/>
   [jQuery]: <http://jquery.com>
   [@tjholowaychuk]: <http://twitter.com/tjholowaychuk>
   [express]: <http://expressjs.com>
   [AngularJS]: <http://angularjs.org>
   [Gulp]: <http://gulpjs.com>

   [PlDb]: <https://github.com/joemccann/dillinger/tree/master/plugins/dropbox/README.md>
   [PlGh]: <https://github.com/joemccann/dillinger/tree/master/plugins/github/README.md>
   [PlGd]: <https://github.com/joemccann/dillinger/tree/master/plugins/googledrive/README.md>
   [PlOd]: <https://github.com/joemccann/dillinger/tree/master/plugins/onedrive/README.md>
   [PlMe]: <https://github.com/joemccann/dillinger/tree/master/plugins/medium/README.md>
   [PlGa]: <https://github.com/RahulHP/dillinger/blob/master/plugins/googleanalytics/README.md>
