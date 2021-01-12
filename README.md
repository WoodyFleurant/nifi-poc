<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Thanks again! Now go create something AMAZING! :D
-->



<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->



<!-- PROJECT LOGO -->
<br />
<p align="center">

  <h3 align="center">Nifi Proof of concept</h3>

  <p align="center">
    An Nifi proof of concept containing templates as examples
    <br />
    <a href="https://github.com/othneildrew/Best-README-Template"><strong>Read the article on Medium »</strong></a>
    <br />
    <br />
  </p>
</p>



<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#license">License</a></li>
  </ol>
</details>


<!-- GETTING STARTED -->
## Getting Started

### Prerequisites

You should install docker and docker compose on your local machine and port 8091 and 8010 should be available

<!-- USAGE EXAMPLES -->
## Usage

Run
```
docker-compose up
```

Then you can access the ui at localhost:8091/nifi and import the templates available under templates folder
To do so inside the Operate window, click on the 'upload template' button and upload both template files.
After that you can add them in your canevas, dragging the templates icon located in the top bar.
You should also activate all controller services. To do so, right click in your canevas, then click configure.
Under "Controller services" tab enable all controllers by clicking on the lightning icon.
After that you can start all the processors.

To trigger the "Receiving and sending HTTP calls" workflow, you need to send an http request, you can do so using curl

```
curl --header "Content-Type: application/json" --request POST --data '{"breed":"hound"}' localhost:8010/contentListener
```

<!-- LICENSE -->
## License

Distributed under the GNU GPL v3 License. See `LICENSE` for more information.



