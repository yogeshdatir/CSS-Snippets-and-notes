Use: To make html page responsive by changing styles according to the media types/devices. Promotes mobile-first approach for UI/UX development.

Note: The contents in square brackets "[]" are optional.

Syntax:

  ```css
  @media [not|only] mediatype[,mediatype] and (mediafeature) [and|or|not (mediafeature)]) {
    CSS-Code;
  }
  ```
  
Examples:
  ```css
  #sidebar ul li a {
    color: #900;
    text-decoration: none;
    padding: 3px 0; 
    display: block;
  }

  @media all and (min-width: 1001px) {
    #sidebar ul li a:after {
      content: " (" attr(data-email) ")";
      font-size: 11px;
      font-style: italic;
      color: #666;
    }
  }

  @media all and (max-width: 1000px) and (min-width: 700px) {
    #sidebar ul li a:before {
      content: "Email: ";
      font-style: italic;
      color: #666;
    }
  }

  @media all and (max-width: 699px) and (min-width: 520px), (min-width: 1151px) {
    #sidebar ul li a {
      padding-left: 21px;
      background: url(../images/email.png) left center no-repeat;
    }
  }
  ```

Bootstrap media queries:

  ```css
  // Extra small devices (portrait phones, less than 576px)
  // No media query for `xs` since this is the default in Bootstrap

  // Small devices (landscape phones, 576px and up)
  @media (min-width: 576px) { ... }

  // Medium devices (tablets, 768px and up)
  @media (min-width: 768px) { ... }

  // Large devices (desktops, 992px and up)
  @media (min-width: 992px) { ... }

  // Extra large devices (large desktops, 1200px and up)
  @media (min-width: 1200px) { ... }
  ```

Techniques to employ responsive design:

  1. Use Javascript to serve relevant CSS files
  2. Use media=”” tag within the header <link>
  3. **Use @media within the CSS file**
  4. Use a mixture of all the above.
