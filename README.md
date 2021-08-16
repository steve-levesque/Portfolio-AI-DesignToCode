<!-- Repo's Banner -->
![Portfolio-AI-DesignToCode](https://user-images.githubusercontent.com/42849270/123730421-520f5d80-d864-11eb-8bd8-db0886fcfd0f.png)



<!-- Shield Badges -->
[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]



<!-- Description of the Project -->
## About
![header2](https://user-images.githubusercontent.com/42849270/123861178-e0332480-d8f4-11eb-851e-915fe8db6f6a.png)

### Introduction
DesignToCode is a project aiming to show a brief example of AI's use in web development to automate tedious and repititive tasks such as the conversion of the idea (Design) into  a real website (Code). This is the HTML and CSS programming respectively.

In summary, computer vision is used to analyse a wireframe to parse all its useful components like text to shapes into computable data for the website to be generated from.

Below, the steps will be explained separately and in order to show the life cycle from the drawing to the HTML/CSS generated website.

No training is necessary for the given examples, only the needed programs. (unless Tesseract is set to work on another language than English or if it is not powerful enough)

All steps in the workflow could be potentially replaced with alternatives and even be refactored.

**NB: This project is not made to create semantically and/or production ready websites.**


### Workflow
The lifecycle of this project has been made by steps which contain its own responsability in order to make it easier to understand and follow.

Here is a brief list with a picture below :
1. Wireframe Drawing.
2. Optical Character Recognition (OCR)
3. Shape Recognition
4. Data Parsing
5. Data Mapping
6. Website Generation

![about_flow](https://user-images.githubusercontent.com/42849270/123883032-0fa65900-d916-11eb-81b8-b222dd556f52.png)

#### Wireframe Drawing
This is the part with the most human interaction. The user will draw a website in a wireframe nomenclature with a few rules such as:
- A picture is represented with a box containing a "X" in it covering the full area.

  ![image](https://user-images.githubusercontent.com/42849270/123886397-577cae80-d91d-11eb-9beb-ea5a6c12178d.png)
  
- An element's type is specified at the top-left or bottom-right most corner from the inside or the outside.

  ![image](https://user-images.githubusercontent.com/42849270/123886109-bbeb3e00-d91c-11eb-8ddc-e863b8f2b324.png)
  ![image](https://user-images.githubusercontent.com/42849270/123886116-bf7ec500-d91c-11eb-839f-eecd1638c05c.png)
  ![image](https://user-images.githubusercontent.com/42849270/123886122-c3aae280-d91c-11eb-8bd1-048acfac48d0.png)
  
- It is not necessary to draw everything perfectly at the pixel close, but the margin of error should not be above 10 pixels for each side of a shape.


#### Optical Character Recognition (OCR)
When the wireframe is done properly, the OCR with Tesseract-OCR and Python will find the words written on it.

The result is then given as a dictionnary to get every parameters such as the coordinates, text and percentage of accuracy.

The accepted percentage must be well balanced. Elsewhere, words could be missing (too high %) or they could not make much sense (too low %).


#### Shape Recognition
It is the same principle than step 2., but there is a different code logic to get the shapes instead of the words.

With more form detections, it is possible to have less words on the wireframe. By example, the picture shape does not need to have an annotation since it can be recognized without ambiguities.


#### Data Parsing
All dictionnaries from step 2 and 3 are parsed into better formats.


#### Data Mapping
The data is mapped together to have all the information in one place.

The data about characters and shapes are put together to have distinct elements that can be computed into the website.


#### Website Generation
With the data parsed and mapped, the only step left is to generate the elements and create the website.

This part will analyse the data to get what specifications an element has in the HTML and CSS aspect.

When it is completed, the elements are arranged together in the respective sheets and the index page can be launched in your favorite browser.



<!-- Repo's Content Tree -->
## Directories and Files
<details open>
  <summary><b>Project's Tree</b></summary>
    
  ``` bash
    |  |- wireframes
    |- .gitignore             #
    |- LICENSE                #
    |- README.md              # This file
    |- requirements.txt       #
  ```
</details>


<!-- Getting Started -->
## Installation
For this project to work, some programs needs to be installed with the required Python libraries:
- Python 3.x
- Jupyter Notebook (optional, but necessary for the notebooks)
- Tesseract-OCR

``` bash
pip install -r requirements.txt
```

All imports are on the notebooks. The notebooks must be executed in order (4-..., 5-..., 6-..., with 1,2,3 that are optional) with read/write permission on the sub-directories and files of the project.

**NB: The default path of Tesseract may not work for your environment. If so, you may have to find the executable and chahnge the path to yours.**

``` bash
// Default path
pytesseract.pytesseract.tesseract_cmd = r'C:\Program Files\Tesseract-OCR\tesseract.exe'
```



## How to Execute
The most simple way to run the project is to use Jupyter Notebook and run all cells of each notebooks in order. The .csv files should be generated almost instantly with the given examples.

It is important to do it in order and wait for the csv file creation because they are reused as the workflow continues.



<!-- Contribution -->
## Contribution

Contributions are always welcome, thank you for you time. Here are the steps to do so.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/MyContribution`)
3. Commit your Changes (`git commit -m 'Add MyContribution'`)
4. Push to the Branch (`git push origin feature/MyContribution`)
5. Open a Pull Request



<!-- License -->
## License

See the `LICENSE` file at the root of the project directory for more information.



<!-- Acknowlegements and Sources -->
## Acknowlegements and Sources
Readings of articles and projects
- https://github.com/emilwallner/Screenshot-to-code
- https://emilwallner.medium.com/how-you-can-train-an-ai-to-convert-your-design-mockups-into-html-and-css-cc7afd82fed4
- https://github.com/tonybeltramelli/pix2code
- https://arxiv.org/abs/1705.07962
- https://github.com/harvardnlp/im2markup
- https://fahmisalman.medium.com/an-easy-way-of-creating-text-localization-and-detection-in-tesseract-ocr-24cc89ed6fbc
- https://towardsdatascience.com/create-simple-optical-character-recognition-ocr-with-python-6d90adb82bb8

Programs
- https://github.com/tesseract-ocr/tesseract
- https://jupyter.org/install
- https://www.python.org/downloads/



<!-- md links & imgs -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/steve-levesque/Portfolio-AI-DesignToCode.svg?style=for-the-badge
[contributors-url]: https://github.com/steve-levesque/Portfolio-AI-DesignToCode/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/steve-levesque/Portfolio-AI-DesignToCode.svg?style=for-the-badge
[forks-url]: https://github.com/steve-levesque/Portfolio-AI-DesignToCode/network/members
[stars-shield]: https://img.shields.io/github/stars/steve-levesque/Portfolio-AI-DesignToCode.svg?style=for-the-badge
[stars-url]: https://github.com/steve-levesque/Portfolio-AI-DesignToCode/stargazers
[issues-shield]: https://img.shields.io/github/issues/steve-levesque/Portfolio-AI-DesignToCode.svg?style=for-the-badge
[issues-url]: https://github.com/steve-levesque/Portfolio-AI-DesignToCode/issues
[license-shield]: https://img.shields.io/github/license/steve-levesque/Portfolio-AI-DesignToCode.svg?style=for-the-badge
[license-url]: https://github.com/steve-levesque/Portfolio-AI-DesignToCode/blob/main/LICENSE
