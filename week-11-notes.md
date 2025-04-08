# Week 11 Class Notes

## Common Mistakes

- Not following instruction posted on GitHub
- Not putting in enough time for homework
- Not asking enough questions outside of class time
- Not asking for help outside of class time
- Adding decorative elements in the HTML, not using only CSS
- Using capitals or spaces in css selector names
- Not adding the CSS reset. [Use this code](https://raw.githubusercontent.com/JACGWD/CSS-Reset-Selector/refs/heads/main/reset/simple-css-reset-v2.2.css) at the top of your stylesheet.
- Make sure your .flex-container divs all have **exactly two elements** inside: a \<picture> tag, and either a single \<p> or a \<div> with multiple other tags inside it. This will create two exactly columns. 


## Simplified Page Layout

        @media screen and (min-width: 60rem) {

        section {
            width: 60rem; 
            /* use the width you prefer for the design, but no wider than the min-width set above */

            margin: 3rem auto;
            /* adjust vertical spacing with the first value, 
            center the section tag with auto left/right margins */
        }

        .flex-container {
            display: flex;  
            /* creates two columns */

            column-gap: 1rem;
            /* space between the columns */
        }

        .flex-container picture, 
        .flex-container > p, 
        .flex-container > div {
            flex-basis: 50%; 
            /* makes each column 50% wide */

            /* > means "direct child of", meaning first level descendent: child, not grandchildren */ 
            /* see https://www.w3schools.com/cssref/css_ref_combinators.php */
        }

        .when .flex-container,
        .how .flex-container {
        /*  select "every other" section tag,
            ex: first and third */


            flex-direction: row-reverse;
            /* swap left and right columns */
        }
        

        } /* always comment the closing media query tag
             so you don't delete it by accident */
