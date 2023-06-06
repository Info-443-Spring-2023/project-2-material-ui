[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/ZL2e6lYH)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-718a45dd9cf7e7f842a935f5ebbe5719a5e09af4491e668f4dbf3b35d5cca122.svg)](https://classroom.github.com/online_ide?assignment_repo_id=11093023&assignment_repo_type=AssignmentRepo)

Team Members: Jasper Wang, Justin Zeng, Sachi Figliolini, Lauren Wong

**Forked Project:**
https://github.com/lwong121/info-443-p2-material-ui


# Project 2 Full Report

## Introduction

**Chosen Project:** Material UI

**What is the software system, and what does it do? Give a short (a few sentences is fine) explanation from a user/consumer perspective.**

From a user perspective, this library can be used to help with software development that interacts with React. Its pre-built components with Google design means better affordances for users.

Material UI is a open-source library offering various pre-built React components that implment Google's Material Design. It can be installed through `npm` or `yarn`.

**Who created the software, and who currently "maintains" it? (Was it developed by a large company or an independent developer? Who seems to be in charge of approving changes to its code/architecture?)**

Founded by Olivier Tassinari and Matt Brookes, Open UI is a team responsible for the development and maintenance of material UI with the support and involvement of the community to also make contributions.

**Where can we find more information about the system?**
- Github Project: https://github.com/mui/material-ui
- Official Documentation: https://mui.com/core/


## Development View

### List of Packages and Components

The following lists contain names and descriptions of the main packages and components included in the Material UI Core repository. Material UI Core is a large repository that contains many different packages for various projects and shared functions [^3]. So the first list aims to describe these high-level packages to provide a better sense of the organization of the repository. The second list then dives deeper into the @mui/material package that contains the main MUI React components the provide by breaking them down into groups, describing them at a high-level, and listing related components or sub-components. The @mui/material package is the main package we will be focusing on for the rest of this project.

***Note:** All details about the packages and components came from [^1], [^2], [^3], and [^4].

**MUI Core Packages:**
- @mui/material – Material UI is a React component library containing the main components that implement the Material Design guidelines. This is the main package we will be focusing on for the rest of this project.
- @mui/base – Base UI is a React component library containing the unstyled and basic versions of MUI components to allow for more customization
- @mui/joy – Joy UI is an alternative React component library to @mui/material containing components that implement MUI’s own design principles instead of the ones from Material Design guidelines
- @mui/system – MUI System provides a collection of CSS utilities that provide the default designs and can allow for more customized designs
  - Styled engines: @mui/styled-engine and @mui/styled-engine-sc  – These packages help create a consistent style for components and allows users to further customize them according to their needs
- @mui/codemod – Contains the codemod scripts used for Material UI
- @mui/core-downloads-tracker - Tracker for the number of downloads of the @mui/material and @mui/joy packages and the number of users for @mui/base
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
- Button – Creates a button. Also has different types of buttons to customize:
  - ButtonBase
  - IconButton
  - LoadingButton
- ButtonGroup – Allows users to create groups of buttons for a more compact layout
- Checkbox – Creates a single checkbox
- Fab – Creates a floating action button (FAB) that appears in front of all other content and is usually used for the main action of a page like a plus or edit button
- RadioGroup – Wrapper component to group Radio button components so that users can select one option from a set
  - Radio
- Rating – Creates a series of buttons used to provide ratings
- Select – Creates a dropdown with a list of options that users can select from
  - NativeSelect
- Slider – Creates a slider that allows users to select a value from a range of values on a bar
- Switch – Creates a switch that can toggle a setting on and off
- TextField – Wrapper component to create a complete text field form control that has a label, input, and help text. It has these smaller components to create more customized form inputs:
  - FilledInput
  - FormControl
  - FormHelperText
  - Input
  - InputLabel
  - OutlinedInput
- Additional form components for more customization:
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
- List – Creates a list of text or images. It also has the following sub-components to allow for more different types of and components in list items.
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
- Dialog – Creates a popup that appears on top of the app content and contains critical information for the user or asks for a decision from the user. It also has the following components to add content to the dialog.
  - DialogActions
  - DialogContent
  - DialogContentText
  - DialogTitle
- 2 types of components showing progress:
  - CircularProgress – Creates a circular loading/progress icon
  - LinearProgress – Creates a linear loading/progress icon
- Skeleton – Creates a placeholder view of content before content and data gets loaded on the page
- Snackbar – Creates a small temporary notification towards the bottom of the screen
  - SnackbarContent

Surfaces:
- Accordion – Creates a tab that can be clicked to hide/show more details in the dropdown. It also has the following sub-components for the content of the tab and dropdown.
  - AccordionActions
  - AccordionDetails
  - AccordionSummary
- AppBar – Creates a navigation/title bar for the app
- Card – Creates a card containing information and actions related to a topic. It also has the following components for the Card's content.
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
- Stepper – Creates a customizable component that shows a user’s progress through a sequence of steps. It also has the following components that can be used to further customize the stepper and add additional content.
  - Step
  - StepButton
  - StepConnector
  - StepContent
  - StepIcon
  - StepLabel
  - MobileStepper
- Tabs – Creates tabs that allow users to navigate between different pages/views. The sub-components listed also allow users to add additional content and functionality.
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
- Hidden – Deprecated component.

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
- Transition Wrapper Components Available:
  - Collapse – Transition wrapper component that makes a component collapse from a starting edge
  - Fade – Transition wrapper component that allows users to fade components from transparent to opaque
  - Grow – Transition wrapper component that makes a component expand and fade in from transparent to opaque
  - Slide – Transition wrapper component that makes a component slide in from the edge of a screen
  - Zoom – Transition wrapper component that makes a component expand outwards
- useMediaQuery() – CSS media query hook that allows components to be rendered depending on whether the given query matches

### Visual Representation
The following is a UML component diagram showing the relationship between the different architechtural components in the material ui system. The arrows represent the relationships between nested components.


![UML component diagram](img/project2_uml.drawio.png)

### Source Code Structure
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


### Approach to Testing and Configuration

**Your report will need to describe the system's approach to testing and configuration. How is automated testing integrated into the code (if at all)? What infrastructure or architecture is needed to enable this testing? Considering how you would "run the tests" and what that would do is a good place to start. Similarly, is there any particular configuration work needed when building or using this system (including e.g., use of particular git branches or tags/labeling)?**

Material UI has many different tests including unit tests, integration tests, end to end (e2e) tests, and visual regression tests. The test folder in root contains e2e tests and visual regression tests while the package folder contains a unit and integration test for each component. For testing, MUI uses tools like @testing-library/react, chai, sinon, mocha, karma, playwright, jsdom, and enzyme. Automated testing is integrated in its visual regression tests where they use playwright to iterate over fixtures and take a screenshot. Each fixture can be described as a rendered UI. This tests the rendering of React components. End to end testing also utilizes playwright and is similar to the visual regression tests where it looks at a single fixture. Focusing on building this system, to add a unit test or integration test, run `yarn t TheUnitInQuestion`, implement the tested behavior, then open a PR  once the test passes. A particular configuration work when adding to this system is that you need to follow. Starting with forking then cloning the repo, then the contributor needs to create a new topic branch, then make a Pull Request (PR). Details here: https://github.com/mui/material-ui/blob/master/CONTRIBUTING.md  To install the mui package, you can do `npm install @mui/material @emotion/react @emotion/styled`.  To run tests, use `yarn test:unit` or `yarn test:unit –grep ComponentName` for unit tests, `yarn docs:api` for checking code formats and lints the repo, `yarn test:karma` to run unit tests in multiple browsers via BrowserStack. To deploy, go to deploy/netlify to render a preview of the docs with your changes. `yarn docs:build` or `yarn docs:export1 usually fails locally. `codecov/project` monitors coverage of the tests.


## Applied Perspective

### Architectural Perspective
We have chosen the Usability perspective from the Rozanski catalog. This perspective considers how the architecture of a system impacts its usability, focusing on end users and UI design. Using this perspective we want to ensure that Material UI supports qualities such as intuitive nagivation, efficient workflows, and user satisfaction. In the following text we will analyze how usability is incorporated into the system's architechture.

### Concerns relevant to System
**Detail which concerns are relevant to your particular system—how does your perspective apply to your chosen software? You should use the listed concerns in the course text as a starting point (you don't need to address all of the concerns in the book; pick 2 or 3 most relevant ones and discuss those explicitly).**
 - There are a couple of usability concerns specific to Material-UI. These concerns stem from the nature of the software system, being a user interface library for web development, and the expectations that come with it.

 - 1. Learnability
 - Material-UI aims to make web development faster and easier, and this includes making the library itself easy to learn. The architecture of the system plays a key role in this aspect. The documentation of the project, which is a reflection of the system's architecture, must be easy to understand to promote learnability. Material-UI has adopted a modular design where components are self-contained and reusable, which promotes learnability by reducing the number of concepts developers need to understand at once.

- 2. Flexibility
- The software must be flexible to cater to various user requirements. The architecture of Material-UI allows for the customization of components. This flexibility is ingrained into the system's architecture by exposing APIs to alter the visual and functional aspects of components.

- 3. Accessibility
- The architecture of the system needs to ensure that the components provided by Material-UI are accessible. The system achieves this by adopting WAI-ARIA (Web Accessibility Initiative – Accessible Rich Internet Applications) standards and providing features like keyboard navigation and text-to-speech capability.


### Activities to Apply the Perspective
**Perform some of the activities mentioned to "apply the perspective". This will often involve analyzing, diagramming, documenting, or assessing some aspect of the system or perspective. The exact format of this section will depend on your specific and chosen activities. Note that an analysis activity can overlap with the discussion of a concern. Your report should include around 2 activities (depending on their size).**
* For example, from an Evolution perspective, you might "Characterize the Evolution Needs" and "Assess the Current Ease of Evolution".

1. Usability Evaluation: Conduct a usability evaluation of specific Material-UI components or the overall UI design. This can involve tasks such as heuristic evaluations, cognitive walkthroughs, or usability testing with representative users. The goal is to identify any usability issues, pain points, or areas for improvement in terms of user interaction, navigation, visual design, or responsiveness.
2. User Flow Analysis: Analyze the user flows and interactions within the Material-UI components used in your application. Identify the key user tasks, actions, and navigation patterns. Create user flow diagrams or storyboards to visualize the sequences of screens and interactions, evaluating the ease of use and clarity of the user journey.

**Activity 1: Usability Evaluation of Material UI's Architecture**

As Rozanski mentions in their book, the usability perspective focuses on evaluating "the ease with which people who interact with the system can work effectively" [^10]. So in most cases, this perspective would be focused on the end users and the design of the UI itself. But since Material UI is a library containing pre-built React components, our discussion will focus on the usability of the library for developers and how the system's architecture supports the usability of the system instead of evaluating the component interfaces. Specifically, we will consider how their architecture makes it easier/harder and more/less effective for developers to integrate the MUI components into their own React apps. The list below discusses how they do this and how they handle some of the common problems and pitfalls mentioned in the reading:

- They strictly follow a set of rules for the design of their API and they clearly define them in their documentation [^7]. For example, they always try to use the `children` prop to do composition with components. They also try to maintain consistent naming conventions for all props and establish standards for how the components handle certain props that are passed in. This is important to ensure consistency in the design of their component API, which makes it easier for developers to understand and use the MUI components in their own projects.
  - Helps developers avoid one of the common problems that Rozanski highlights in [^10], which is creating overly complex systems. They do this by keeping all the components as consistent as possible and clearly defining any rules and exceptions in their documentation.

- They designed their MUI components to adhere to Google's Material Design Principles. This ensures that they follow a widely accepted standard within the design community that aligns with the needs of the users and provide known and tested solutions for certain design problems and contexts. It also helps them maintain consistency and simplify communication about their API design, documentation, and component designs because it is based on the standard set of concepts described in the design principles and it relies on designs that the developers and users would expect, which could be particularly useful for developers already somewhat familiar with the design principles. A good example of this is their responsive UI components that help developers align the designs of their applications with the responsive layouts defined by Material Design [^11].
  - Doing this helps them avoid two of the common problems and pitfalls described by Rozanski in [^10]: failing to bring in non-IT professionals like designers and failing to comply with strict guidelines. This is because they are building these components off of the design expertise of the designers that created the Material Design Principles.

- They follow a component-based architecture (more information in the architectural styles section). So they focus on encapsulating parts of the UI into independent, reusable, and fairly customizable components that can be re-combined to create more complex components. This is important because it helps them keep code related to different elements of the UI separate and consistent, which makes the code more maintainable and usable for developers who want to quickly and effectively get their app up and running.
  - Helps developers follow the main architectural principle that Rozanski highlights in [^10], which is to keep the implementation of the interface separate from the functional processing so that it is easier to make changes quickly and easily in the future.

- They provide clear and easy-to-follow documentation on their web page to describe each component in their API, their props, their use cases, demos of how to use the components, and general guidelines [^1].
  - The documentation on the design and proper usage does not necessarily relate to the architecture of the system. But I included it here because it is still an important element that contributes to the usability of the MUI components for developers by ensuring consistency and clarity.

- Finally, though they do provide extensive documentation and guidelines on how to use the API and the overall architecture is based on common patterns and styles, it is clear that many of it has been designed with the assumption that the developers already have some background knowledge. In particular, they assume that developers using the library are already familiar working with React, component-based architectures, design principles, and common programming concepts. They also don't really provide much explanation of some technical jargon and how exactly the packages interact with each other in the code. So the system might prove to be challenging to use and understand for new developers with less expertise and experience to work with initially.
  - Failing to take into account the capabilities, expertise, and experience of the users is one of the common problems that Rozanski points out in [^10].
   
**Activity 2: User Flow Analysis of Material UI's Website**

![User Storyboard](img/User-Flow-Analysis.jpg)

The first step in identifying key user tasks is to understand the main objectives of the application. The user here would be web developers, front end developers, or react developers who are looking for an UI framework that is compatible with React.
User tasks: 
- Component Exploration and Selection: One of the key user tasks for the Material-UI package is to explore the available components and select the ones that best suit their needs. Users may need to browse through the documentation, view examples, and understand the usage guidelines for each component. The actions involved in this task include searching for specific components, reading documentation, viewing demos, and identifying the appropriate component for integration into their project.

- Installation and Setup: Once users have selected the desired components, the next task is to install and set up the Material-UI package in their development environment. This task involves actions such as installing the package through package managers like npm or yarn, configuring the necessary dependencies, and integrating the components into the project's codebase. The ease of use in terms of installation instructions, clear documentation, and smooth integration can greatly impact the user experience.

- Customization and Styling: Another important task for users is to customize and style the Material-UI components to align with the visual design and branding of their application. This task requires actions like modifying component properties, applying custom styles, and handling component interactions. The ease of use in terms of customization options, theming support, and clear guidelines for styling contribute to a positive user experience.

Next, we need to determine the actions users need to take to complete each task. From the user's perspective, the website has seamless getting started steps that are easy to follow and copy and pastable. The user can then click on specific components to read more. These documentation pages often includes copyable code chunks and interactive demo code chunks for the developer to play around with and see how it would display before implementation. 

Users are able to navigate between different documentation using the navigation bar that is always present on the left with highlighted bold text to contrast the background. It is also intuitively designed to include clear categorization of components, help guides, and customizations. The main navigation menu and breadcrumbs also help users understand their current location within the website.


## Identify Styles & Patterns Used

### Architectural Style

Material UI is a library that provides users with a bunch of prebuilt React components that developers can use to build UIs. These components were designed to be independent, flexible, and reusable building blocks that are easy to combine and interchange to create more complex UI components. So they follow and support a Component-Based architectural style, where each component is clearly defined to handle a specific goal/task or represent an element of the UI and they are loosely coupled and independent components. Additionally, as we have seen from the list of core packages in the development view, the architecture of the system is also split up into different components and packages depending on what their purpose/use is. For example, we have the @mui/material package containing the MUI components themselves and the @mui/system package that focuses on providing the CSS styling for these components. The @mui/material package relies on the @mui/system package to create the default and user-defined styling for all of their components. But they keep the styling code separate from the component code, and ensure that the same code for styling can be used on other components too so they maintain consistency in the design. All of this helps support the separation of concerns, code reusability, modularity, extensibility, and cohesion within the UI of an app using their components [^8].

Since it is just a library of components, Material UI does not really apply any other architectural styles on its own. But the MUI components can be used within other system’s architectures that involve a clearly defined presentation or a UI component, such as the model-view-controller (MVC) architecture and a layered architecture.

In an MVC architecture, the MUI components would act as the View that the user sees and interacts with. If an event handler is applied to the View, the View will be responsible for: (1) keeping the Controller updated on the user’s actions, (2) displaying information to the user according to updates it receives from the Controller, and (3) making additional requests for relevant data and updating accordingly when it gets notified by the Model about changes [^9]. Then as usual, the Controller will be responsible for handling the input from the user and translating it to the rest of the system. The Model will be responsible for the core functionality and data-related logic.

Similarly, in a layered architecture, the MUI components would be part of building the UI in the presentation layer. This layer is responsible for handling all of the user interactions with the application and communicating information between the logic layer and the user.

### Software Design Patterns:

**Your will identify 4 or more design patterns (e.g., OOP Patterns) that are are used in the implementation of your system. (You should find at least 3 different patterns—a single pattern used in 2 different places can both be counted in the required 4). Your report will need to name each pattern being used, then provide an explanation of how the system uses that pattern. Don't just say where the pattern is; explain how this particularly implementation fits the requirements of the pattern. The goal is to demonstrate you understand the pattern's structure and usage.**

### Decorator Pattern
Decorator Pattern involves dynamically adding behaviors or responsibilities to an object by wrapping it with another object of the same interface.
In Material-UI, High order components or HOCs are used to inject certain features or behaviors into components, such as handling theming, managing state, or providing access to certain context or data. These HOCs can be applied to existing components to extend their capabilities without modifying their underlying implementation. This promotes code reusability and modularity by separating concerns and allowing components to be composed with different functionalities. While the concept of enhancing components through HOCs shares some similarities with the Decorator Pattern, it is important to note that the implementation in Material-UI may not strictly adhere to the full structure and principles of the Decorator Pattern.

### Observer Pattern
Context: This pattern is used in Material-UI's theme provider. The ThemeProvider allows child components to react to theme changes. Problem: The objective is to create a system where when one object changes state, all its dependents are notified and updated automatically. In Material-UI, this is particularly useful for theme changes to be propagated throughout the app's components. Solution: Material-UI's ThemeProvider uses the Context API to make the theme available to all child components. When a theme change is triggered, all components that consume the context will re-render with the new theme. This closely follows the Observer Pattern where the ThemeProvider is the Subject and the child components are the Observers.

### Composite Design pattern
The composite design pattern is a pattern that lets you use tree structures to represent hierarchies and treat both individual objects and object compositions the same [^5][^6]. Material UI uses the composite design pattern to create their components because they let you treat the individual objects and object compositions as parts of a whole. For example, to create a `List` component you can compose a list by passing in various `ListItem`s as children. These list items can have any number of other components contained within them like a `ListItemAvatar`, `ListItemText`, or `ListItemButton` to create a tree hierarchy. But despite the fact that there could be many different subtrees (`ListItem`s) with different structures in the list, the `List` component will still treat all of its child `ListItem`s as individual objects instead of  compositions of multiple different objects.

Material UI also does a very good job in creating components that support other systems using the composite design pattern. This is because they prioritize creating consistent and basic low-level components so that they fully maximize their ability to use composition with their components for more complex tree structures [^7].

### Abstract Factory pattern
The Abstract Factory pattern involves families of related product objects without instantiating the classes directly. Material UI implements this design pattern through the different theme providers. The `ThemeProvider` interface is the abstract factory interface in Material-UI as it declares methods for creating different types of theme objects. The problem is that the project needs to supports various themes for the components. Therefore, `ThemeProvider` ensures that all contrete theme factories adhere to a common set of creation methods by creating multiple concrete factory classes such as `createMuiTheme` and `createTheme`. 

## Architectural Assessment

### Open/Close Principle (OCP)
Material-UI adheres to the Open/Closed Principle by providing an extensible framework of reusable components that can be customized and extended through props. Instead of modifying the internal implementation, developers can leverage props to tailor the appearance, behavior, and functionality of components to fit their specific requirements. This approach promotes code reusability, maintainability, and modularity, allowing for the addition of new features without modifying the existing codebase.

### Single Responsibility Principle (SRP)
Material UI follows the Single Responsibility Principle by ensuring that each of the React components they provide have one and only one well-defined purpose within the system. We can see this when we look at how the MUI components are broken down into smaller and more basic sub-components to achieve a single goal or represent a certain element in the user interface [^7] (as shown in the list of components from the development view). Also, as mentioned in the usability evaluation section, they provide clear and consistent interfaces so that developers can easily understand what each component does and how they can use it. As a result, this type of approach helps to make the components more modular so that they are easier to reuse and combine to create more complex and customized components. It also helps make the code easier to maintain, understand, and improve in the future.

Example: Instead of having a single `Card` component handle all the content involved with creating a card, they break it down into smaller individual components such as the `CardHeader`, `CardContent`, and `CardMedia` to represent different parts of the content displayed on a card. These additional components are not required, but they can be used to add more detail. The `Card` component can be further extended by combining it with other components like `Typography` and `Collapse` to create even more complex UI components. From this example, it is clear that they keep each of their components modular so that they serve separate purposes and can be added/removed as needed. Also, keeping the code separate from each other makes it easier to make changes to the code in the future because changing one component does not lead to breaking something else.

### Liskov Substitution Principle (LSP)
LSP states that functions that use pointers or references to base classes must be able to use objects of derived classes without knowing it. This ensures that a derived class will not cause the system to behave differently, eliminating the possibility of errors in the system. After exploring the codebase of Material-UI, it can be concluded that the project adheres to the Liskov Substitution Principle. A specific example can be found in the Button component. This component extends from the ButtonBase component, inheriting properties and methods. Yet, when used in the context of the ButtonBase, it doesn't alter the behavior of the system. This respects LSP because we can substitute ButtonBase with Button and the system will behave as expected.

### Interface Segregation Principle (ISP)
ISP suggests that clients should not be forced to depend on interfaces they do not use. This principle is all about business value and code organization by focusing on the role of an interface. In the context of Material-UI, ISP is adhered to effectively. Material-UI follows a modular design structure and the components are segregated properly based on their responsibilities. For instance, TextField and Select components have their own specific implementations and are not bloated with unnecessary methods. This clear segregation provides developers the flexibility to import and use only the components and their associated interfaces that are necessary for their implementation, thus adhering to the ISP.

### Dependency Inversion Principle (DIP)
DIP posits that high-level modules should not depend on low-level modules. Both should depend on abstractions. Similarly, abstractions should not depend on details; details should depend on abstractions. Material-UI also follows this principle quite well. All the components are written in such a way that they depend on abstractions rather than concrete implementations. A prime example can be seen in the theme implementation of Material-UI. All the components depend on the abstract theme provided by the ThemeProvider and not on the specific implementation of the theme. This allows developers to create their own themes without having to modify the internal component code.

## System Improvement

Around 4-5 refactoring steps (at the scope defined by Martin Links to an external site). For example, you might apply Extract Function a couple of times, Move Functions, or even Parameterize Functions. This is probably the easiest approach, and is most relevant to the architecture of the project.
A larger reorganization (e.g., at the module level—breaking up a module into smaller pieces, or moving functionality between modules) can "count double" in terms of refactorings. So doing 2-3 of those would be sufficient.
You will need to justify why each refactoring is needed and an improvement on the architecture. Consider perhaps places that the system could better follow the design principles you discussed in the previous section.**

### Refractoring
Refactored Box, Card, and the className components.
* For `Box.js` and `Box.test.js`, the `ClassNameGenerator` import was optimized to import from the `@mui/utils` package. Originally, the import was importing the `className` component.
* The `className` component was removed because of redundancy. The component file only had 1 file and 1 import statement, it was also only referenced by `Box` and `Box test`.
* The `Card` component had a couple refactoring steps.
  * Instead of importing all the modules with `import * as module`, we switched to using named imports (import { module }). This change improves code readability and maintainability by explicitly stating which modules are being imported and used. It also helps to avoid potential naming conflicts and makes it easier to understand the dependencies of the module.
  * We removed unused imports such as `chainPropTypes`, `styled`, `useThemeProps`, and `unstable_composeClasses`. This cleanup improves the codebase by eliminating unnecessary dependencies and reducing potential confusion or conflicts.
  * The `styled` function is now imported from the `@mui/system` package. This is because the styled function was moved to the `@mui/system` package in recent versions of Material-UI.
  * We created a separate `CardRoot` component that extends the `Paper` component and overrides its styles. This change follows the principle of separation of concerns, allowing the `Card` component to focus on its specific functionality while delegating the style-related concerns to the `CardRoot` component.
  * Additionally in the refactored code, the `forwardRef` function is placed inside the `Card` component definition for better code organization and readability. This ensures that the `Card` component is defined as a `forward-ref` component and clarifies the intent of using the `ref` prop.
  * The `sx` prop has also been updated to import `PropTypes` from the `prop-types` package and added to the Card `propTypes` definition. This ensures that the `sx` prop is properly type-checked and documented.
  * In the `useUtilityClasses` hook, the slot value for the root has been changed from an array ['root'] to a string 'root' for consistency. The `slot` property in styled expects a string value representing the slot name.
  * In the `useThemeProps` call, the `name` property has been updated to `MuiCard` to align with the component name. This is a convention used by Material-UI for theme-related functionality. In the `CardRoot` component, the `ref` prop has been moved outside the `ownerState` spread to separate it from the other props. This ensures that the `ref` is correctly passed to the underlying `Paper` component.


### Bug Fix: [Stack] misalignment
**Github Issue:** https://github.com/mui/material-ui/issues/37381

**Bug Fix Commit:** https://github.com/lwong121/info-443-p2-material-ui/commit/61c77cac69f43aa6a61a4e3ed5129905abf169ac

**Bug Description:**

The original issue on github mentioned that the elements (in this case the `FormControlLabel` components) in the stack were not properly aligned and there was additional space in front of the first switch in the stack. But after inspecting the elements further, the margin of the first element was actually shifted to the left by 11px while all of the other elements were aligned on a 0 margin. So there seemed to be some inconsistency with how they were applying the styles to the child elements of the stack.

Current alignment issue:

![alignment bug](img/bug-fix-issue.jpg)

```
// Code to reproduce
// App.cs
<Stack direction="column" spacing={1}>
  <FormControlLabel
    value="Auto Seek"
    control={<Switch color="primary" />}
    label="Auto skip 1"
  />
  <FormControlLabel
    value="Auto Seek"
    control={<Switch color="primary" />}
    label="Auto skip 2"
  />
  <FormControlLabel
    value="Auto Seek"
    control={<Switch color="primary" />}
    label="Auto skip 3"
  />
</Stack>
```

**Background:**

In the `Stack.js` file included in the `@mui/material` package, they call the `createStack()` function to create a Stack component. This function is defined in the `createStack.tsx` file in the `@mui/system` package, where they define the `StackRoot` component that acts as the base component for the stack with all the default styling and is created using the `defaultCreateStyledComponent()` function. That function then takes in a `style()` function to create styles for all the child elements of the stack component using the current state of the Stack (defined in `ownerState`). In the `style()` function, they define another function called `styleFromPropValue()` to generate styles for each child element. Here, it uses the CSS selector `& > :not(style) + :not(style)` to apply a `margin: 0` and additional margins based on the specified direction from the user (in this case they use the `"column"` direction).

```
// Source of the problem
// createStack.tsx
const styleFromPropValue = (propValue: string | number | null, breakpoint?: Breakpoint) => {
  ...
  return {
    '& > :not(style) + :not(style)': {
      margin: 0,
      [`margin${getSideFromDirection(
        breakpoint ? directionValues[breakpoint] : ownerState.direction,
      )}`]: getValue(transformer, propValue),
    },
  };
};
```

**Solution:**

The cause of this issue was the CSS selector `'& > :not(style) + :not(style)'` that applied to all direct child elements apart from the first non-`style` child element and any `style` elements. So the solution was to make the `margin:0` CSS rule apply to all direct non-`style` child elements using the `'& > :not(style)'` selector and have the other direction-dependent margin CSS rule apply to all elements apart from the first element using the same `'& > :not(style) + :not(style)'` selector. This is so that we could keep consistency with the left margin for all child components and ensure that the first component does not have the extra top margin when the user specifies the amount of spacing they want between components in the stack.

```
// Fixed code
// createStack.tsx
const styleFromPropValue = (propValue: string | number | null, breakpoint?: Breakpoint) => {
  ...
  return {
    '& > :not(style)': {
      margin: 0,
    },
    '& > :not(style) + :not(style)':{
      [`margin${getSideFromDirection(
        breakpoint ? directionValues[breakpoint] : ownerState.direction,
      )}`]: getValue(transformer, propValue),
    },
  };
};
```

Result from change:

![alignment bug solution](img/bug-fix-result.jpg)

The `Stack.test.js` file in the `@mui/system` package was also updated to make sure the changes made are correct and can be tested in the future. All tests for styling the stack component pass.

![alignment bug test cases passing](img/bug-fix-tests.jpg)

### Feature Improvement
...

### Test Cases
For the test case, I focused on the Select function, which has the automated test cases stored in the Select.test.js file.

1. First test case: Testing the Select component with a null default value
 - Reason: The Select component might be initialized with a null default value in certain scenarios, and this case does not seem to be covered in the existing test cases. This test is necessary to ensure that the component behaves correctly when initialized with a null value.

 ```
 test('renders Select with null default value without crashing', () => {
  const { getByRole } = render(
    <Select
      defaultValue={null}
      onChange={jest.fn()}
    >
      <MenuItem value="item1">Item 1</MenuItem>
      <MenuItem value="item2">Item 2</MenuItem>
    </Select>,
  );

  expect(getByRole('button')).toBeInTheDocument();
});
```

2. Second test case: Testing the Select component when the 'onChange' handler is null

Reason: There might be scenarios where the 'onChange' handler isn't provided, and the component needs to be able to handle such cases gracefully. This case does not seem to be covered in the existing test cases.
 
 ```
 test('renders Select with null onChange handler without crashing', () => {
  const { getByRole } = render(
    <Select
      defaultValue="item1"
      onChange={null}
    >
      <MenuItem value="item1">Item 1</MenuItem>
      <MenuItem value="item2">Item 2</MenuItem>
    </Select>,
  );

  const selectComponent = getByRole('button');
  fireEvent.mouseDown(selectComponent);
  expect(selectComponent).toBeInTheDocument();
});
```
3. Third test case: Testing the Select component with no child MenuItem components

Reason: There could be cases where the Select component does not have any child 'MenuItem' components due to data unavailability or other reasons. The component should be able to handle such situations gracefully.

 ```
 test('renders Select without any MenuItem children without crashing', () => {
  const { getByRole } = render(
    <Select
      defaultValue="item1"
      onChange={jest.fn()}
    >
    </Select>,
  );

  expect(getByRole('button')).toBeInTheDocument();
});
```



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