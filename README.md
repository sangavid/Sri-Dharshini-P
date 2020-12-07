# Sri-Dharshini-P
Pdf viewer

npm i create-react-app --save-dev
npx create-react-app my-app
cd my-app
npm run start


import React, { Component } from 'react';
import './App.css';

class App extends Component {
  render() {
    return (
      <div className="App">

      </div>
    );
  }
}

export default App;

html, body, #root, .App {
  width: 100%;
  height: 100%;
}

import React from 'react';

export default class PDFViewer extends React.Component {

  render() {
    return (
      <div id='viewer' style={{ width: '100%', height: '100%' }}>
        Hello world!
      </div>
    )
  }
}

import React, { Component } from 'react';
import './App.css';
import PDFViewer from './components/PDFViewer/PDFViewer';

class App extends Component {
  render() {
    return (
      <div className="App">
        <PDFViewer />
      </div>
    );
  }
}

export default App;

export default class PDFJs {
  init = () => {
    
  }
}

export default class PDFJs {
  init = (source, element) => {
    
  }
}

import React, { Component } from 'react';
import './App.css';
import PDFViewer from './components/PDFViewer/PDFViewer';
import PDFJSBackend from './backends/pdfjs';

class App extends Component {
  render() {
    return (
      <div className="App">
        <PDFViewer 
          backend={PDFJSBackend}
          src='/myPDF.pdf'
        />
      </div>
    );
  }
}


import React from 'react';

export default class PDFViewer extends React.Component {
  constructor(props) {
    super(props);
    this.viewerRef = React.createRef();
    this.backend = new props.backend();
  }

  render() {
    return (
      <div ref={this.viewerRef} id='viewer' style={{ width: '100%', height: '100%' }}>

      </div>
    )
  }
}

import React from 'react';

export default class PDFViewer extends React.Component {
  constructor(props) {
    super(props);
    this.viewerRef = React.createRef();
    this.backend = new props.backend();
  }

  componentDidMount() {
    const { src } = this.props;
    const element = this.viewerRef.current;

    this.backend.init(src, element);
  }
  

  render() {
    return (
      <div ref={this.viewerRef} id='viewer' style={{ width: '100%', height: '100%' }}>

      </div>
    )
  }
}
fullscreen



export default class PDFJs {
  init = (source, element) => {
    const textNode = document.createElement('p');
    textNode.innerHTML = `Our PDF source will be: ${source}`;

    element.appendChild(textNode);
  }
}
