### Creating a new Vaadin Element

1. Clone this repo

        git clone git@github.com:vaadin/vaadin-side-menu-skeleton.git new-element-name

2. When in the `new-element-name` folder, replace all `vaadin-side-menu` and `VaadinSideMenu` occurrences with your new element name.

        perl -pi -e 's,vaadin-side-menu,new-element-name,g' *.* demo/* test/* src/* theme/*/*
        perl -pi -e 's,VaadinSideMenu,NewVaadinSideMenuName,g' *.* demo/* test/* src/* theme/*/*

3. Rename the element

        mv vaadin-side-menu.html new-element-name.html
        mv src/vaadin-side-menu.html src/new-element-name.html
        mv theme/lumo/vaadin-side-menu.html theme/lumo/new-element-name.html

4. Check that everything works all right

        npm install
        bower install
        polyserve

  And check that everything works:
  
  - http://localhost:8080/components/new-element-name/index.html
  - http://localhost:8080/components/new-element-name/demo/index.html
  - http://localhost:8080/components/new-element-name/test/index.html

5. Remove this README file since it is not needed any more.

        rm README_CREATE_NEW.md

5. Finally, initialize git so as we have an empty history for our `<new-element-name>`

        rm -rf .git
        git init
        git add * .??*
        git commit -m 'First Commit' -a

