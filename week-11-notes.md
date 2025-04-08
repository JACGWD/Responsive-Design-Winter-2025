# Week 11 Class Notes

## Common Mistakes

- No decoration in HTML, only use CSS
- No capitals or spaces in css selector names.flex-container
- Missing reset
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
            flex-direction: row-reverse;
            /* swap left and right columns */
        }
        /* select every other section tag  */

        } /* always comment the closing media query tag */
