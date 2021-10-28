

## How To Use 🔧

From your command line, first clone Dopefolio:

```bash
# Clone this repository
$ git clone https://github.com/rammcodes/dopefolio

# Go into the repository
$ cd dopefolio

# Remove current origin repository
$ git remote remove origin
```

<br/>

Then you can install the dependencies

Using NPM:

```bash
# Install dependencies
$ npm install

# Listen to changes in CSS Preprocessor files ( SASS files )
$ npm run compile:scss
```

Once you run `npm run compile:scss`, then open the `index.html` inside your favorite browser or using the live server extension.

<br>

---

<br>

## Template Instructions:

## Step 1 - STYLES

Make sure you have started the SASS to CSS compilation by running

```bash
$ npm run compile:scss
```

Change the color theme of the website.

Go to `sass/abstracts/_variables.scss` and change the value of this sass variable called `$themeClrPrimary` to your preferred HEX color.

```scss
// Default value
$themeClrPrimary: #0062b9;
```

**NOTE**: I highly recommend to checkout the [Dopefolio Playground Link](https://dopefolio-playground.netlify.app) to test the template with different colors and see which color do you like the most.

<br/>

---

<br/>

## Step 2 - Homepage

Go to `/index.html` and fill your information, there are 6 sections:

### Header of Homepage

- On `.header__logo-img`, Add your own Image, Better if the background of the image is transparent so the background can match the theme color. To remove the background of your image, you can visit remove.bg where you can upload your image and it will remove the background of it.
- On `.header__logo-sub`, Add your own Name.

```html


### Hero Section of Homepage

- On `.heading-primary`, put your custom title.
- On `.text-primary`, put a short description about yourself.
- On `.home-hero__social-icon-link`, fill the href attribute with a link related to your social media account.


```

### About Section

- On `.heading-sec__sub`, put a short description about the section.
- On `.about__content-details-para`, put your details here and use `<strong></strong>` tag to highlight specific keywords.
- On `.skills__skill`, mention your skill one by one.


### Projects

- On `.heading-sec__sub`, put a short description about the section.
- `.projects__row` is the row for each project in your portfolio.
- One `.projects__row` for each project in your portfolio ( so for example, if you have 3 projects then you need 3 `.projects__row` one by one).

- Inside each `projects__row`, there are 4 main elements.

  - Project Image is located at `.projects__row-img` where you can add the URL for your project mockup/image. You can use websites like [Media Modifier](https://mediamodifier.com/) and [SmartMockups](https://smartmockups.com) to generate mockups for free. Just make sure to crop the extra white space around your mockup so the mockups can look bigger and the size of the mockup file will be less.

  - `.projects__row-content-title` is where you need to add your Project title.
  - `.projects__row-content-desc` is where you need to add a short 2-3 lines description of your project. As there's going to be a separate page for each project so there you can add all the details for each project on the specific project page.
  - The Anchor tag ( **Case Study** button) on press will take you to the details page for each project ( For example: If you click the **Case Study** button of Project 1 then it will take you to the `project-1.html` file where you will have all the details about that particular project).

Currently, I have already added a separate for each project ( considering there are 3 projects ) the file names are `project-1.html`, `project-2.html`, and `project-3.html`. They all contain the same code only the project title, description and image will change. If you like to add more projects then you can just create a new file for it and paste the same code that we have in `project-1.html` as the code is going to be the same and the only thing that you need to change is the data inside each project.



### Contact Section

- On `.heading-sec__sub`, put a short description about the section.
- `.contact__form-field` is the field inside form. Currently, there are 3 fields but you can add more fields as per your need but just make sure to change the name of **label** and **input/textarea** inside it.

If you like to know how to submit forms so you can receive the form details in your email then highly recommend using **formspree.io** as it's easier to set up and free to use. If you are using **Netlify** to host the site then Netlify has an inbuilt form receiver which you can use instead of **formspree**.





### Footer Section

- Inside h4 tag with the class `heading heading-sm text-lt` add your name.
- On `.main-footer__short-desc` put a short description about yourself.
- On Anchor tag inside `.main-footer__social-cont`, fill the href attribute with a link related to your social media account.


## Step 3 - Project Page

Each project will have its own Page. The project page will have important details about the project like the Project Title, Description, Technologies, Project Links, etc.

### Project Hero Section

- On `.heading-primary` add the Project Title.
- On `.text-primary` add a short description about the Project.
- On Anchor Tag that says **Live Link** with class `btn btn--bg`, add the Project Live Link as the value for the href attribute.



### Project Details Section

- On `.project-details__showcase-img`, change the value of **src** to the location/link of Project Mockup.
- On `.project-details__desc-para` to add a detailed paragraph describing your project. Use multiple `.project-details__desc-para` elements for multiple paragraphs.
- On `.skills` mention the skills that were used to build the project inside `.skills__skill` to mention each skill.
- On Anchor Tag that says **Live Link** with class `btn btn--med btn--theme project-details__links-btn`, add the Project Live Link as the value for the href attribute.
- On Anchor Tag that says **Code Link** with class `btn btn--med btn--theme-inv project-details__links-btn`, add the Project's Code Link ( Repository Link ) as the value for the href attribute.



## Deployment 📦

Once you have done with your setup. You need to put your website online!

I highly recommend to use [Netlify](https://netlify.com) to achieve this on the EASIEST WAY

Whenever you wanna host a new site on Netlify. You will need to press the **Create New Site** button from the Netlify's dashboard once you login into Netlify.

Once you press the **Create Site Button** then you will have to follow the 3 steps:

1. You will have to select your Github account.

2. Then select the Repository which you wanna host, in this case its your Portfolio website ( Clone of Dopefolio )

3. In the 3rd step, you will have to modify the **Site settings and deploy**, keep everything as it is but just make sure to modify the **Build command** and set its value to **npm run build** and then modify the **Publish directory** and set its value to **/** as shown in the  **image** below

