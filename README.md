[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/ZL2e6lYH)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-718a45dd9cf7e7f842a935f5ebbe5719a5e09af4491e668f4dbf3b35d5cca122.svg)](https://classroom.github.com/online_ide?assignment_repo_id=11093023&assignment_repo_type=AssignmentRepo)

Team Members: Jasper Wang, Justin Zeng, Sachi Figliolini, Lauren Wong

# Checkpoint 1

**Forked Project:**
https://github.com/lwong121/info-443-p2-material-ui

**Chosen Project:** Material UI
- Github Project: https://github.com/mui/material-ui
- Documentation: https://mui.com/core/

**What is the software system, and what does it do?** Give a short (a few sentences is fine) explanation from a user/consumer perspective. From a user perspective, this library can be used to help with software development that interacts with React. Its pre-built components with Google design means better affordances for users.

Material UI is a open-source library offering various pre-built React components that implment Google's Material Design. It can be installed through `npm` or `yarn`.

**Who created the software, and who currently "maintains" it?** (Was it developed by a large company or an independent developer? Who seems to be in charge of approving changes to its code/architecture?)

Founded by Olivier Tassinari and Matt Brookes, Open UI is a team responsible for the development and maintenance of material UI with the support and involvement of the community to also make contributions.



# Project 2 Full Report

## Development View

### List of Packages and Components

The following lists contain names and descriptions of the main packages and components included in the Material UI Core repository. Material UI Core is a large repository that contains many different packages for various projects and shared functions [^3]. So the first list aims to describe these high-level packages to provide a better sense of the organization of the repository. The second list then dives deeper into the @mui/material package that contains the main MUI React components by describing the them at a high-level and listing related components.

***Note:** All details about the packages and components came from [^1], [^2], [^3], and [^4].

**MUI Core Packages:**
- @mui/material – Material UI is a React component library containing the main components that implement the Material Design guidelines. This is the main package we will be focusing on in this project.
- @mui/base – Base UI is a React component library containing the unstyled and basic versions components to allow for more customization
- @mui/joy – Joy UI is an alternative React component library to @mui/material containing components that implement MUI’s own design principles instead of the ones from Material Design guidelines
- @mui/system – MUI System provides a collection of CSS utilities that can allow for more custom designs
  - Styled engines: @mui/styled-engine and @mui/styled-engine-sc  – These packages help create a consistent style for components and allows users to further customize them according to their needs
- @mui/codemod – Contains the codemod scripts used for Material UI
- @mui/core-downloads-tracker
- @mui/docs – Contains the building blocks used for Material UI documentation
- @mui/envinfo – Prints information on current environment related to the Material UI packages to the console
- @mui/icons-material – Contains Google Material Icons that have been converted to SvgIcon components
- @mui/material-next – Contains components that are currently being improved to replace the @mui/material components
- @mui/lab – Contains components that are currently being developed and tested, so they are not yet ready for actual use as an official MUI component
- @mui/private-theming - Contains the main React theme context that is shared with @mui/styles and @mui/material
- @mui/styles - Contains the legacy styling solution for Material UI and is no longer in use
- @mui/types - Contains the utility types used by MUI
- @mui/utils - Contains the shared utilities that are used by MUI packages
- eslint-plugin-material-ui – Contains the custom eslint rules used for Material UI
- Typescript-to-proptypes - Contains an API to convert TypeScript definitions to PropTypes using the TypeScript Compiler API
- Waterfall - Contains a set of utility functions for handling async/await


**Material UI Components in @mui/material:**

Inputs:
- Autocomplete – Creates a text input box with built-in autocomplete functionality that shows suggestions on a panel
- Button – Creates a button
  - ButtonBase
  - IconButton
  - LoadingButton
- ButtonGroup – Allows users to create groups of buttons for a more compact layout
- Checkbox – Creates a single checkbox
- Fab – Creates a floating action button (FAB) that appears in front of all other content and is usually used for the main action of a page like a plus or edit button
- RadioGroup – wrapper to group Radio components so that users can select one option from a set
  - Radio
- Rating – Creates a series of buttons used to provide ratings
- Select – Creates a dropdown with a list of options that users can select from
  - NativeSelect
- Slider – Creates a slider that allows users to select a value from a range of values on a bar
- Switch – Creates a switch that can toggle a setting on and off
- TextField – Wrapper component to create a complete form control that has a label, input, and help text. It has these smaller components to create more customized form inputs:
  - FilledInput
  - FormControl
  - FormHelperText
  - Input
  - InputLabel
  - OutlinedInput
- Additional Form Components:
  - FormControlLabel – Adds extra labels to radio, switch, and checkbox control components in a form
  - FormGroup – Groups control components together to create a more compact layout
  - FormLabel – Adds a label to a form, input field, or FormGroup component
- ToggleButton – Creates a button that can be toggled as one of the options in a ToggleButtonGroup component
  - ToggleButtonGroup

Data Display:
- Avatar – Creates an avatar with an image, letter, or icon
  - AvatarGroup – Allows users to create groups of Avatar components to make it more condensed
- Badge – Adds a small badge to the top right of a component, similar to one you might see on an app icon when you have messages
- Chip – Creates a compact and multi-purpose element that can represent an action, attribute or input
- Divider – Creates a thin line to group or separate content
- Icon – Acts as a wrapper for custom font icons
  - SvgIcon
- Material Icons - Basic icons provided by Material UI
- List – Creates a list of text or images
  - ListItem
  - ListItemAvatar
  - ListItemButton
  - ListItemIcon
  - ListItemSecondaryAction
  - ListItemText
  - ListSubheader
- Table – Creates fully customizable table to display sets of data
  - TableBody
  - TableCell
  - TableContainer
  - TableFooter
  - TableHead
  - TablePagination
  - TableRow
  - TableSortLabel
- Tooltip – Creates a text label to identify a component when users hover over, focus on, or tap an element
- Typography – Allow users to apply any default set of font styles to some text for better consistency throughout the app

Feedback:
- Alert – Creates an alert on the the page with different severity levels: error, warning, info, and success
  - AlertTitle
- Backdrop – Create dimmed layer over the app to draw attention to an element on the screen
- Dialog – Creates a popup that appears on top of the app content and contains critical information for the user or asks for a decision from the user
  - DialogActions
  - DialogContent
  - DialogContentText
  - DialogTitle
- Progress:
  - CircularProgress – Creates a circular loading/progress icon
  - LinearProgress – Creates a linear loading/progress icon
- Skeleton – Creates a placeholder view of content before content and data gets loaded on the page
- Snackbar – Creates a small temporary notification towards the bottom of the screen
  - SnackbarContent

Surfaces:
- Accordion – Creates a tab that can be clicked to hide/show more details in the dropdown
  - AccordionActions
  - AccordionDetails
  - AccordionSummary
- AppBar – Creates a navigation/title bar for the app
- Card – Creates a card containing information and actions related to a topic
  - CardActionArea
  - CardActions
  - CardContent
  - CardHeader
  - CardMedia
- Paper – Creates a customizable component that resembles some of the physical properties of a piece of paper

Navigation:
- BottomNavigation – Creates a navigation bar at the bottom on a screen with 3-5 possible actions
  - BottomNavigationAction – Allows users to add the individual actions on a BottomNavigation bar component
- Breadcrumbs – Creates a path of links that shows the location of a page according to the structure of the website and allows for navigation between pages
- Drawer – Creates a navigation sidebar that allows users to access extra actions and functionality on a menu to the left or right of the screen
  - SwipeableDrawer
- Link – Creates a link that can be further customized with theme colors and typography styles
- Menu – When a user performs an action on a component like a button, it creates a temporary list of options a user can choose from
  - MenuItem
  - MenuList
- Pagination – Creates a series of buttons that allow users to navigate between a range of pages
  - PaginationItem
- SpeedDial – Displays 3-6 related actions when a Fab component is clicked
  - SpeedDialAction
  - SpeedDialIcon
- Stepper – Creates a customizable component that shows a user’s progress through a sequence of steps
  - Step
  - StepButton
  - StepConnector
  - StepContent
  - StepIcon
  - StepLabel
  - MobileStepper
- Tabs – Creates tabs that allow users to navigate between different pages/views
  - TabContext
  - TabList
  - TabPanel
  - Tab
  - TabScrollButton

Layout:
- Box – Acts like a wrapper component that allows users to add CSS code to a component
- Container – Layout component used for centering content horizontally
- Grid – Allows users to create a responsive grid layout that can adapt to variables like screen size and orientation
  - Unstable_Grid2 (Grid v2NEW)
- Stack – Container component used to organize elements vertically or horizontally
- ImageList – Component to create a collection of images in an organized format
  - ImageListItem
  - ImageListItemBar
- Hidden – Deprecated component

Utils:
- ClickAwayListener – Component being moved to Base UI
- CssBaseline – Adds some basic CSS styling to keep the overall design consistent and organized
  - ScopedCssBaseline
- Modal – Component that displays its children node in on top of a Backdrop component and can be used on multiple children to keep the focus on a particular element on the screen
- NoSsr – Component being moved to Base UI
- Popover – Component that displays content on top of other content on the screen and blocks scrolling and clicking away
- Popper – Component that displays content on top of other content on the screen and allows scrolling and clicking away
- Portal – Component being moved to Base UI
- TextareaAutosize – Component being moved to Base UI
- Transitions Available:
  - Collapse – Transition wrapper component that makes a component collapse from a starting edge
  - Fade – Transition wrapper component that allows users to fade components from transparent to opaque
  - Grow – Transition wrapper component that makes a component expand and fade in from transparent to opaque
  - Slide – Transition wrapper component that makes a component slide in from the edge of a screen
  - Zoom – Transition wrapper component that makes a component expand outwards
- useMediaQuery() – CSS media query hook that allows components to be rendered depending on whether the given query matches


**Source Code Structure**
- Material-UI is a popular React UI framework that implements Google's Material Design. It includes a variety of pre-built components like buttons, cards, dialogs, forms, and more, making it easier to build beautiful and consistent interfaces.
- /packages: The Material-UI codebase is organized into packages, which are each responsible for different aspects of the framework. For example, there might be separate packages for core components, system utilities, and lab components (components that are still being tested and not yet fully stable).
- 1.1. /material-ui: This directory usually contains the core of the library - the React components. These components include Buttons, Cards, Dialogs, etc. They are typically organized into their respective folders.
- 1.2. /material-ui-lab: This is where newer components are tested before they are moved to the core package.
- 1.3. /material-ui-system: This package contains utility functions and helpers for style functions.
- 1.4. /material-ui-utils: This is a collection of utility modules required by Material-UI components.
- /docs: This directory contains the source code for the Material-UI documentation. The documentation is itself a showcase of Material-UI components and serves as a valuable resource for developers learning how to use the framework.
- /test: This is where all the test files reside. The tests ensure that changes to the code do not break existing functionality.
- /examples: This directory contains example projects using Material-UI.
- Root Files: At the root of the project, you might find configuration files for various tools such as Babel, ESLint, Prettier, etc., used for transpiling, linting, and formatting the code respectively. You would also find the package.json file which lists all the project dependencies.
- /scripts: This directory would typically contain build scripts, test scripts, and possibly scripts for generating new components or other code.
- Other files including README.md, SECURITY.md still need further analysis and will be implemented in the next updates.



**Your report will need to describe the system's approach to testing and configuration. How is automated testing integrated into the code (if at all)? What infrastructure or architecture is needed to enable this testing? Considering how you would "run the tests" and what that would do is a good place to start. Similarly, is there any particular configuration work needed when building or using this system (including e.g., use of particular git branches or tags/labeling)?**

Material UI has many different tests including unit tests, integration tests, end to end (e2e) tests, and visual regression tests. The test folder in root contains e2e tests and visual regression tests while the package folder contains a unit and integration test for each component. For testing, MUI uses tools like @testing-library/react, chai, sinon, mocha, karma, playwright, jsdom, and enzyme. Automated testing is integrated in its visual regression tests where they use playwright to iterate over fixtures and take a screenshot. Each fixture can be described as a rendered UI. This tests the rendering of React components. End to end testing also utilizes playwright and is similar to the visual regression tests where it looks at a single fixture. Focusing on building this system, to add a unit test or integration test, run `yarn t TheUnitInQuestion`, implement the tested behavior, then open a PR  once the test passes. A particular configuration work when adding to this system is that you need to follow. Starting with forking then cloning the repo, then the contributor needs to create a new topic branch, then make a Pull Request (PR). Details here: https://github.com/mui/material-ui/blob/master/CONTRIBUTING.md  To install the mui package, you can do `npm install @mui/material @emotion/react @emotion/styled`.  To run tests, use `yarn test:unit` or `yarn test:unit –grep ComponentName` for unit tests, `yarn docs:api` for checking code formats and lints the repo, `yarn test:karma` to run unit tests in multiple browsers via BrowserStack. To deploy, go to deploy/netlify to render a preview of the docs with your changes. `yarn docs:build` or `yarn docs:export1 usually fails locally. `codecov/project` monitors coverage of the tests.

## Applied Perspective

**Detail which concerns are relevant to your particular system—how does your perspective apply to your chosen software? You should use the listed concerns in the course text as a starting point (you don't need to address all of the concerns in the book; pick 2 or 3 most relevant ones and discuss those explicitly).**
 - Evolution: Magnitude/dimensions of change: Since its creation, Material-UI has undergone significant changes. The development team has made updates to improve the library's performance, features, and maintainability. Some of these changes include transitions from class-based to functional components and Hooks and incorporation of TypeScript, reflecting the evolution in the broader JavaScript ecosystem. Likelihood/timescale for change: Material-UI, as an open-source project, is updated frequently. Looking at the project’s history, major versions have been released approximately every two years. The project follows semantic versioning, which helps users to anticipate the impact of updates. Changes driven by external factors: The primary external factor driving changes in Material-UI is the development of React and JavaScript as a whole. Changes in the underlying technologies necessitate updates in Material-UI to maintain compatibility and to leverage new features and improvements. User feedback and trends in web design also play a role in shaping the library's evolution.
- Security - further implementation needed.11
- Performance - further implementation needed.



**Perform some of the activities mentioned to "apply the perspective". This will often involve analyzing, diagramming, documenting, or assessing some aspect of the system or perspective. The exact format of this section will depend on your specific and chosen activities. Note that an analysis activity can overlap with the discussion of a concern. Your report should include around 2 activities (depending on their size).**
* For example, from an Evolution perspective, you might "Characterize the Evolution Needs" and "Assess the Current Ease of Evolution".

1. Usability Evaluation: Conduct a usability evaluation of specific Material-UI components or the overall UI design. This can involve tasks such as heuristic evaluations, cognitive walkthroughs, or usability testing with representative users. The goal is to identify any usability issues, pain points, or areas for improvement in terms of user interaction, navigation, visual design, or responsiveness.

**Activity 1: Usability Evaluation of Material UI's Architecture**

As Rozanski mentions in their book, the usability perspective focuses on evaluating "the ease with which people who interact with the system can work effectively" [^10]. In most cases, this perspective would be focused on the end users and the design of the UI itself. But since Material UI is a library containing pre-built React UI components, our discussion will mostly focus on the usability of the library for developers and how the system's architecture supports usability. Specifically, we will consider how their architecture makes it easier/harder and more/less effective for developers to integrate the MUI components into their own React apps.

- They provide clear and easy-to-follow documentation on their web page to describe each component in their API, their props, their use cases, demos of how to use the components, and general guidelines [^1].
  - This documentation on the design and usage does not really relate to the architecture of the system. But it is still an important element that contributes to the usability of their MUI components for developers because it ensures consistency.

- They strictly follow a set of rules for the design of their API and they clearly define them in their documentation [^7]. For example, they always try to use the `children` prop to do composition with components. They also try to maintain consistent naming conventions for all props and establish standards for how the components handle certain props that are passed in. This is important to ensure consistency in the design of their component API, which makes it easier for developers to understand and use the MUI components.

- They designed their MUI components to adhere to Google's Material Design Principles. This ensures that they follow a widely accepted standard within the design community that aligns with the needs of the users and provide known and tested solutions for certain design problems and contexts. It also helps them maintain consistency in and simplify communication about their API design, documentation, and component designs because it is based on the standard set of concepts described in the design principles and it relies on designs that the developers and users would expect, which could be particularly useful for developers already somewhat familiar with the design principles. A good example of this is their responsive UI components that help developers align the designs of their applications with the responsive layouts defined by Material Design [^11].
  - Helps them avoid two of the common problems and pitfalls described by Rozanski in [^10]: failing to bring in non-IT professionals like designers and failing to comply with strict guidelines.

- They follow a component-based architecture (more information in the architectural styles section). So they focus on encapsulating parts of the UI into independent, reusable, and fairly customizable components that can be reused and re-combined to create more complex components. This is important because it helps them keep code related to different elements of the UI separate and consistent, which makes it more maintainable and usable for developers who want to quickly and effectively get their app up and running.
  - Helps developers follow the main architectural principle that Rozanski highlights in [^10], which is to keep the implementation of the interface separate from the functional processing so that it is easier to make changes quickly and easily in the future.

- Though they do provide extensive documentation and guidelines on how to use the API and the overall architecture is based on common patterns and styles, it is clear that many of it has been designed with the assumption that the developers already have some background knowledge. In particular, they assume that developers using the library are familiar working with React, component-based architectures, design principles, and common programming concepts. So it might prove to be challenging to use for new developers with less expertise and experience to work with initially, which is one of the common problems that Rozanski points out in [^10].


2. User Flow Analysis: Analyze the user flows and interactions within the Material-UI components used in your application. Identify the key user tasks, actions, and navigation patterns. Create user flow diagrams or storyboards to visualize the sequences of screens and interactions, evaluating the ease of use and clarity of the user journey.

## Identify Styles & Patterns Used

### Architectural Style

Material UI is a library that provides users with a bunch of prebuilt React components that developers can use to build UIs. These components were designed to be independent, flexible, and reusable building blocks that are easy to combine and interchange to create more complex UI components. So they follow and support a Component-Based architectural style, where each component is clearly defined to handle a specific goal/task or represent an element of the UI. This helps support the separation of concerns, code reusability, modularity, extensibility, and cohesion within the UI of an app using their components [^8].

Since it is just a library of components, Material UI does not really apply any other architectural styles on its own. But the MUI components can be used within other system’s architectures that involve a clearly defined presentation or a UI component, such as the model-view-controller (MVC) architecture and a layered architecture.

In an MVC architecture, the MUI components would act as the View that the user sees and interacts with. If an event handler is applied to the View, the View will be responsible for: (1) keeping the Controller updated on the user’s actions, (2) displaying information to the user according to updates it receives from the Controller, and (3) making additional requests for relevant data and updating accordingly when it gets notified by the Model about changes [^9]. Then as usual, the Controller will be responsible for handling the input from the user and translating it to the rest of the system. The Model will be responsible for the core functionality and data-related logic.

Similarly, in a layered architecture, the MUI components would be part of building the UI in the presentation layer. This layer is responsible for handling all of the user interactions with the application and communicating information between the logic layer and the user.

### Software Design Patterns:

Your will identify 4 or more design patterns (e.g., OOP Patterns) that are are used in the implementation of your system. (You should find at least 3 different patterns—a single pattern used in 2 different places can both be counted in the required 4). Your report will need to name each pattern being used, then provide an explanation of how the system uses that pattern. Don't just say where the pattern is; explain how this particularly implementation fits the requirements of the pattern. The goal is to demonstrate you understand the pattern's structure and usage.

 ### Decorator Pattern
 Decorator Pattern involves dynamically adding behaviors or responsibilities to an object by wrapping it with another object of the same interface.
 In Material-UI, High order components or HOCs are used to inject certain features or behaviors into components, such as handling theming, managing state, or providing access to certain context or data. These HOCs can be applied to existing components to extend their capabilities without modifying their underlying implementation. This promotes code reusability and modularity by separating concerns and allowing components to be composed with different functionalities. While the concept of enhancing components through HOCs shares some similarities with the Decorator Pattern, it is important to note that the implementation in Material-UI may not strictly adhere to the full structure and principles of the Decorator Pattern.

 ### Factory Pattern
 This pattern is used in the styles portion of the system. Material-UI needs to create styles that can be easily tweaked based on themes, props, and states. To solve this problem, Material-UI uses a factory function to create styles. In essence, the function takes a theme and returns a style object that depends on that theme. This effectively allows the creation of custom styles based on different themes using the same factory function.



### Composite Design pattern

The composite design pattern is a pattern that lets you use tree structures to represent hierarchies and treat both individual objects and object compositions the same [^5][^6].

Material UI uses the composite design pattern to create their components because they let you treat all individual objects and object compositions the same. For example, to create a `List` component you can compose a list by passing in various `ListItem`s as children. These list items can have any number of other components contained within it like a `ListItemAvatar`, `ListItemText`, or `ListItemButton` to create a tree hierarchy. But despite the fact that there could be many different subtrees with different structures in the list, the `List` component will still treat all of its `ListItem`s as an individual object instead of a composition of multiple different objects.

Material UI also does a very good job in creating components that support other systems using the composite design pattern. This is because they prioritize creating consistent and basic low-level components so that they can fully maximize the composition capabilities of their components [^7].


## Architectural Assessment

### Open/Close Principle (OCP)
Material-UI adheres to the Open/Closed Principle by providing an extensible framework of reusable components that can be customized and extended through props. Instead of modifying the internal implementation, developers can leverage props to tailor the appearance, behavior, and functionality of components to fit their specific requirements. This approach promotes code reusability, maintainability, and modularity, allowing for the addition of new features without modifying the existing codebase.

### Single Responsibility Principle (SRP)

Material UI follows the Single Responsibility Principle by ensuring that each of the React components they provide have one and only one well-defined purpose within the system. The MUI components are broken down into smaller and more basic components to achieve a single goal or represent a certain element in the user interface [^7]. They also provide clear and consistent interfaces so that developers can easily understand what each component does and how they can use it. As a result, this type of approach helps to make the components more modular so that they are easier to reuse and combine to create more complex and customized components. It also helps make the code to maintain, understand, and improve in the future.

Examples: Instead of having a single `Card` component handle all the the elements involved with creating a card, they break it down into smaller individual components such as the `CardHeader`, `CardContent`, and `CardMedia` to represent different parts of the content displayed on a card. This can be further extended by combining it with other components like `Typography` and `Collapse` to create even more complex UI components.

## System Improvement

Around 4-5 refactoring steps (at the scope defined by Martin Links to an external site). For example, you might apply Extract Function a couple of times, Move Functions, or even Parameterize Functions. This is probably the easiest approach, and is most relevant to the architecture of the project.
A larger reorganization (e.g., at the module level—breaking up a module into smaller pieces, or moving functionality between modules) can "count double" in terms of refactorings. So doing 2-3 of those would be sufficient.
You will need to justify why each refactoring is needed and an improvement on the architecture. Consider perhaps places that the system could better follow the design principles you discussed in the previous section.


## Footnotes
[^1]: Component API available at: https://mui.com/

[^2]: Documentation on packages: https://mui.com/material-ui/guides/understand-mui-packages/

[^3]: Core packages offered by Material UI: https://mui.com/blog/mui-product-comparison/

[^4]: Material UI github packages: https://github.com/mui/material-ui/tree/master/packages

[^5]: Composite Design Pattern: https://refactoring.guru/design-patterns/composite

[^6]: Composite Design Pattern: https://learning.oreilly.com/library/view/design-patterns-elements/0201633612/ch04.html#:-:text=Object%20Structural%3A%20Composite

[^7]: Documentation on how they created the API: https://mui.com/material-ui/guides/api/

[^8]: Component-Based Architecture: https://www.mendix.com/blog/what-is-component-based-architecture/#:~:text=Component%20architecture%20is%20a%20framework,requiring%20modification%20of%20other%20components.

[^9]: MVC Architecture: https://learning.oreilly.com/library/view/pattern-oriented-software-architecture/9781118725269/OEBPS/9781118725269_c02a.htm#:-:text=Model-View-Controller,interface%20and%20the%20model.

[^10]: Usability Perspective: https://learning.oreilly.com/library/view/software-systems-architecture/9780132906135/ch29.html#:-:text=The%20Usability%20Perspective

[^11]: Responsive UI Components: https://mui.com/material-ui/guides/responsive-ui/