# General Questions

### What actions have you personally taken on recent projects to increase maintainability of your code?
Despite being the only Front-end engineer on the my latest project, I decided to introduce [Prettier](https://prettier.io/) to the build; the project will likely change-hands at some point, and implementing formatting rules which aren't catered entirely to my tastes should make for a more team-friendly codebase.

I also strive to provide useful comments, meaningful identifiers, and sensible component abstraction on each build I am a part of.

### Can you describe your workflow when you create a web page?
It depends on the build stage; if I had developed all the required UI elements for the composition then I would simply ask for the content to be provided, either from an API or a static source. 

If it was the very start of the build I would spend my time developing all the UI elements depicted in the design workfiles.

---
### If you have 5 different stylesheets, how would you best integrate them into the site?
It would depend entirely on the available budget, and the protocol.

__Limited Time__
If using `http` then I would simply concatenate all individual stylesheets into one CSS file using a build task, however if utilising `http2` I would likely leave as is. 

Regardless of the protocol, I would work towards removing any redundant or duplicate rulesets and declarations across the various stylesheets.


__Good Time__
My preference would be to introduce a pre-processor and abstract the existing styles into component `sass` or `less` files - this would allow me to remove any redundant or duplicate rulesets and declarations, and provide better maintainability moving forward.

If working with `http2` I would look at alternate ways to serve the stylesheets; we don't need to be serving a monolithic stylesheet if we can serve multiple, modular stylesheets across the superior protocol.

---
### Explain the importance of standards and standards bodies.
---
### What is Flash of Unstyled Content? How do you avoid FOUC?
---
### Explain some of the pros and cons for CSS animations versus JavaScript animations.
