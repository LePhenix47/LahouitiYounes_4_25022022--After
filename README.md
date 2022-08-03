# LahouitiYounes_4_25022022--After
So this is the optimised version of the website for the SEO and the accessibility for the 4th project of OpenClassrooms 


GitHub pages: https://lephenix47.github.io/LahouitiYounes_4_25022022--After/

A LOT of changes were made, here are the most important ones:

I found :
9 accessibility issues related to the technical optimization of the site
7 SEO issues related to on-page SEO and technical structure

A) Accessibility
1. Use of image for text
For the perceptibility of the site, it is important to avoid putting images for the text because: it makes the site slower to load, it cannot be selected, making the selection of the text as well as the translation impossible. And it's flagged as a "Blackhat" technique by Google.
Moreover these images have a bad use of the "class" attribute and supposed to be used to change the style of the element

It is imperative to use block semantic tags for the text (<p>, <q> or <blockquote>…)

I replaced the <img/> tags with a <blockquote> as well as a link to the article of the client who posted the opinion or an <h2> with the text of the image

Sources:
WCAG 1.4.5
 
 

2.Responsive design
The responsive design has flaws in mobile, there is the text image which is truncated or which does not fill the whole container and finally there are the lists which are a little truncated in the footer. What harms UX and impacts accessibility, here is a screenshot of the problem

Always code your site on mobile first because 58% of Google users are on mobile, and designing for tablets, laptops and desktops becomes easier

I removed the text for the images and added a padding for the lists
Source: WCAG 5.2.2 and Google


3. Lack of ARIA attributes in tags
There are a lot of missing ARIA 'role', 'aria-label' or 'aria-labelledby' (careful because aria-labelledby works like a <label for="..">) tags in the HTML code of the site
People using the alternative display will not be able to find their way around the page correctly

These tags must be added because there are tags to which there are no default attributes to add HTML, a title attribute or an alternative textual description
I added a role to all semantic tags like <main>, <ul>, <nav>, <footer>… as well as an aria-label=''region'' for sections and an aria-labelledby in buttons as well as in forms

Source: WCAG 2.4.6

4. Misuse of alt= attributes
The alt attribute must be used to provide an alternative textual description for image content and links (visible and non-textual content), or they contain the keywords, which affects accessibility since a person using a reader screen won't have clear information about the non-text element.
In addition, it is a so-called “Black hat” technique, which risks penalizing the site

You must use alt tags to give an alternative textual description as well as a title that gives more information about an element

I replaced the content of the alt attribute with an alternative textual description for the images as well as for the links

Source :


5. Failure to respect the maximum contrast of 3:1 for headlines and minimum 4.5:1 for text
There are 29 elements that do not meet the 4.5:1 image-to-text contrast, which confuses users as they can no longer see the content properly and risks making the text indistinguishable and unreadable
Ensure contrast for text is at least 4.5:1 and at most 3:1 for large text with the WAVE Web accessibility evaluation tool or with aXe DevTools
I changed the background color of the text, I also added a secondary color (craberry) for the buttons and a tertiary color (Pansy) for the footer

Source: WCAG AA 1.4.3

7. Illegible text and imperceptible/unpredictable contact page
The text is unreadable because the font is too small (<16px) and the title of the contact page has the title "page2", which can confuse the user since he cannot predict which page he is going to to bring

Make sure the text is at least 16px or 1.6 EM in size

I changed the text size to 16px and changed the title of "page2" to "Contact Us"

8. Photo images with inappropriate format and size too large
2 of the 4 photo images have a BITMAP (.bmp) format which does not compress the images making it very large, for that matter
