# Dialogflow for Web *v2*
This is a mobile-friendly Web Application for [Dialogflow V2](https://dialogflow.com).  
For a live demo, [check this](https://mishushakov.github.io/dialogflow-web-v2/).

# Installation

## Requirements

- NodeJS & NPM (or Yarn)
- Dialogflow V2 Project (for V1, use this [old repo](https://github.com/mishushakov/dialogflow-web))

## Set up Dialogflow Gateway (backend)
To connect this UI with Dialogflow, you need to use a backend server.

- [Dialogflow Gateway API](https://github.com/narVidhai/Dialogflow-Gateway-Server) - Host this server and get the hosted URL.

## Setup
Clone this repo first and `cd` into it.

### Get the dependencies

- Using npm: `npm i`
- (Or) Using yarn: `yarn`

### Connect your Agent

Open `src/Config/index.js` and change the `API_URL` variable to your Dialogflow Gateway API that you hosted.

The logo, agent name, description and available languages are fetched from your Dialogflow project. Change them there and it will sync to the UI.

## Serving the application
To `serve` the web application (development purpose):

- Using npm: `npm run serve`
- (Or) Using yarn: `yarn serve`

Your browser should open and redirect to `localhost:8080`. You can also give a `--port` argument to serve at specific port.

## Building for production
Your app will be bundled to the `dist` directory

- Using npm: `npm run build`
- (Or) Using yarn: `yarn build`

<hr/>
<hr/>

## UI Features
Note: This is an unofficial Web Integration

- Dark Mode & [Theming](#theming)
- Voice Input and Speech Feedback (with SSML)
- [Docker](./Dockerfile) and [Kubernetes](./k8s) support
- [Rich-component](https://developers.google.com/assistant/conversational/rich-responses), Webhook and Actions on Google Support ([demo](https://mishushakov.github.io/dialogflow-web-v2/))
- Floating Widget for embedding on websites ([repo and demo](https://github.com/mishushakov/df-btn))
- Based on Vue, Webpack, Babel and PostCSS
- Lightweight (build is <50KB gzipped)
- Free and fully Documented
- Recommended by [Dialogflow](https://twitter.com/Dialogflow/status/923976390201847809) and [MadeWithVueJS](https://twitter.com/MadeWithVueJS/status/1130147606666063875)

## Theming
You can make a custom theme for Dialogflow for Web v2, according to the specification:

![Theme Dialogflow for Web v2](https://svgur.com/i/HVW.svg)

To apply the variables, open `src/Style/Theme.sass` and change them in the `\:root` selector

You can also optimize your theme for Dark-mode-enabled clients within the same file and selector under the `@media (prefers-color-scheme: dark)`

Please note, when adding new languages, you may have to translate some of the UI as well (`translations.json` in `src/Translations`)
