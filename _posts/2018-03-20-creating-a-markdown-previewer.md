---
Layout: 
Title:  "Creating a Markdown-Previewer"
Date:   2018-03-20
---


## Overview

Before building this program, I had to go read-up on markdown so that I get an understanding on what it is and how it works. According to Wikipedia markdown is a lightweight markup language with plain text formatting syntax,created to convert a simple text fomat to HTML and the type of that document/file being **.md**.

This blog post is base on how I went about building my **Markdown-previewer**, so I will be explaining the steps that I took finish this task.

## Requirements/Instructions:

## What I used to build this App:

* first I globally installed React's **create-react-app**, then on my terminal, I entered **create-react-app [my-app]**. My app is a folder that contains everything required to build a react app.

* using my terminal I cd to my-app, and installed another node_module called **marked**.

* then went in to /my-app/**src** and created two files, index.js and index.css. Index.js being where I write my javascript and index.css for my styling.

## My css:

    textarea{/* position: relative; */
        float: left;
        width:400px;
        height: 500px;
        margin-bottom:7%;
    }
    .iframe{
        /* position: relative; */
        float: right;
        width:800px;
        height: 500px;
        border: 4px solid;
        border-color: #333;
        background-color:#555;
        color:#ccc;
        margin-bottom:7%;
    }
    .header{
        text-align: center;
        font-size: 50px;
        margin-bottom:7%;
        margin-top:3%;
    } 

## React javascript code:

    import React from 'react';
    import ReactDOM from 'react-dom';
    import './index.css';
    import marked from 'marked'
    class MarkdownViewer extends React.Component {
        constructor(props) {
            super(props);
            this.state = { value: '' }
        }

        handleChange(e) {
            this.setState({ value: e.target.value })
        }
        render() {
            console.log(this.state)
            return (
                <div className='row'>
                    <div className='col-sm-12 header'>Markdown Previewer</div>
                    <textarea className='col-sm-11' id='input' onChange={this.handleChange.bind(this)} />
                    <div className='col-sm-11 iframe' dangerouslySetInnerHTML={{ __html: marked(this.state.value) }}></div>

                </div>
            )
        }
    }



    ReactDOM.render(<MarkdownViewer />, document.getElementById('root'));




