<template>
    <style>
:root {
    --bodyfontFamily: 'Poppins', sans-serif;
    --bodyfontSize: 16px;
    --bodyfontColor: transparent;
    --bodyfontWeight: inherit;
    --bodyfontHeight: 2;
    --bodyfontPadding: inherit;
    --bodyBackground: light;
    --bodybackgroundPosition: center;
    --bodybackgrooundRepeat: repaet;
    --bodybackgroundSize: cover;
     
}

.bodySection {
    font-family: var(--bodyfontFamily);
    font-size: var(--bodyfontSize);
    color: var(--bodyfontColor);
    font-weight: var(--bodyfontWeight);
    line-height: var(--bodyfontHeight);
    padding: var(--bodyfontPadding);
    background: var(--bodyBackground);
    background-repeat: var(--bodybackgrooundRepeat);
    background-position: var(--bodybackgroundPosition);
    background-size: var(--bodyfontSize);
}

:root {
    --sectionMargin: 10px;
    --sectionBackgroundColor: transparent;
    --sectionBackgroundPosition: vertical;
}

section {
    margin: var(--sectionMargin);
    background-color: var(--sectionBackgroundColor);
    background-position: var(--sectionBackgroundPosition);
}

:root {
    --h1fontFamily: 'Poppins', sans-serif;
    --h1fontSize: 16px;
    --h1fontColor: transparent;
    --h1fontWeight: inherit;
    --h1fontHeight: 2;
    --h1fontStyle: normal;
    --h1LetterSpacing: 2px;
    --h1TextDeoration: inherit;
    --h1TextTransform: Inherit;
    --h1textShadow: none;
}

h1 {
    font-family: var(--h1fontFamily);
    font-size: var(--h1fontSize);
    line-height: var(--h1fontHeight);
    font-weight: var(--h1fontWeight);
    font-style: var(--h1fontStyle);
    text-transform: var(--h1TextTransform);
    text-decoration: var(--h1TextDeoration);
    letter-spacing: var(--h1LetterSpacing);
    text-shadow: var(--h1textShadow);
    color: var(--h1fontColor);
}

:root {
    --h2fontFamily: 'Poppins', sans-serif;
    --h2fontSize: 16px;
    --h2fontColor: transparent;
    --h2fontWeight: inherit;
    --h2fontHeight: 2;
    --h2fontStyle: normal;
    --h2LetterSpacing: 2px;
    --h2TextDeoration: inherit;
    --h2TextTransform: Inherit;
    --h2textShadow: none;
}

h2 {
    font-family: var(--h2fontFamily);
    font-size: var(--h2fontSize);
    line-height: var(--h2fontHeight);
    font-weight: var(--h2fontWeight);
    font-style: var(--h2fontStyle);
    text-transform: var(--h2TextTransform);
    text-decoration: var(--h2TextDeoration);
    letter-spacing: var(--h2LetterSpacing);
    text-shadow: var(--h2textShadow);
    color: var(--h2fontColor);
}

:root {
    --h3fontFamily: 'Poppins', sans-serif;
    --h3fontSize: 16px;
    --h3fontColor: transparent;
    --h3fontWeight: inherit;
    --h3fontHeight: 2;
    --h3fontStyle: normal;
    --h3LetterSpacing: 2px;
    --h3TextDeoration: inherit;
    --h3TextTransform: Inherit;
    --h3textShadow: none;
}

h3 {
    font-family: var(--h3fontFamily);
    font-size: var(--h3fontSize);
    line-height: var(--h3fontHeight);
    font-weight: var(--h3fontWeight);
    font-style: var(--h3fontStyle);
    text-transform: var(--h3TextTransform);
    text-decoration: var(--h3TextDeoration);
    letter-spacing: var(--h3LetterSpacing);
    text-shadow: var(--h3textShadow);
    color: var(--h3fontColor);
}

:root {
    --h4fontFamily: 'Poppins', sans-serif;
    --h4fontSize: 16px;
    --h4fontColor: transparent;
    --h4fontWeight: inherit;
    --h4fontHeight: 2;
    --h4fontStyle: normal;
    --h4LetterSpacing: 2px;
    --h4TextDeoration: inherit;
    --h4TextTransform: Inherit;
    --h4textShadow: none;
}

h4 {
    font-family: var(--h4fontFamily);
    font-size: var(--h4fontSize);
    line-height: var(--h4fontHeight);
    font-weight: var(--h4fontWeight);
    font-style: var(--h4fontStyle);
    text-transform: var(--h4TextTransform);
    text-decoration: var(--h4TextDeoration);
    letter-spacing: var(--h4LetterSpacing);
    text-shadow: var(--h4textShadow);
    color: var(--h4fontColor);
}

:root {
    --linkColor: #aaaaaa !important;
    --linkHoverColor: transparent;
    --linkTextDecoration: inherit;
    --linkHoverTextDecoration: normal;
}

a {
    color: var(--linkColor);
    text-decoration: var(--linkTextDecoration);
}

a:hover {
    color: var(--linkHoverColor);
    text-decoration: var(--linkHoverTextDecoration);
}

:root {
    --buttonFontFamily: 'Poppins', sans-serif;
    --buttonFontSize: 15px;
    --buttonFontWeight: inherit;
    --buttonLetterSpacing: 1px;
    --buttonFontColor: transparent ;
    --buttonTextTransform: inherit;
    --buttonBorder: 1px solid transparent;
    --buttonBorderRadius: 5px;
}
button{
    font-family: var(--buttonFontFamily);
    font-size: var(--buttonFontSize);
    font-weight: var(--buttonFontWeight);
    color: var(--buttonFontColor);
    letter-spacing: var(--buttonLetterSpacing);
    text-transform: var(--buttonTextTransform);
    border: var(--buttonBorder);
    border-radius: var(--buttonBorderRadius);
}
:root{
    --buttonPrimarycolor : white;
    --buttonPrimarycolorhover: black;
    --buttonPrimaryOutline: black;
    --buttonPrimaryOutlinehover: black;
    --buttonPrimaryBorder: black;
    --buttonPrimaryBorderhover: black;
}
button.btn-primary{
    color: var(--buttonPrimarycolor);
    outline-color:  var(--buttonPrimaryOutline) ;
    border-color: var(--buttonPrimaryBorder);
}
button.btn-primary:hover{
    color: var(--buttonPrimarycolorhover);
    outline-color:  var(--buttonPrimaryOutlinehover) ;
    border-color: var(--buttonPrimaryBorderhover);
}
:root{
    --buttonSecondarycolor : white;
    --buttonSecondarycolorhover: black;
    --buttonSecondaryOutline: black;
    --buttonSecondaryOutlinehover: black;
    --buttonSecondaryBorder: black;
    --buttonSecondaryBorderhover: black;
}
button.btn-Secondary{
    color: var(--buttonSecondarycolor);
    outline-color:  var(--buttonSecondaryOutline) ;
    border-color: var(--buttonSecondaryBorder);
}
button.btn-Secondary:hover{
    color: var(--buttonSecondarycolorhover);
    outline-color:  var(--buttonSecondaryOutlinehover) ;
    border-color: var(--buttonSecondaryBorderhover);
}
:root{
    --otherBordercolor: black;
    --otherBorder2xcolor: black;
    --otherTextPrimary: black;
    --otherTextSecondary: black;
}
</style>
</template>