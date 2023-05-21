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

### List of Components
*All details about the components came from[^1], [^2], [^3], and [^4].

**Core Modules:**
- @mui/material – Material UI is a React component library containing the main components that implement the Material Design guidelines. This is the main component we will be focusing on in this project.
- @mui/base – Base UI is a React component library containing the unstyled and basic versions components to allow for more customization
- @mui/joy – Joy UI is an alternative React component library to @mui/material containing components that implement MUI’s own design principles instead of the ones from Material Design guidelines
- @mui/system – MUI System provides a collection of CSS utilities that can allow for more custom designs
  - Styled engines: @mui/styled-engine and @mui/styled-engine-sc  – These packages help create a consistent style for components and allows users to further customize them according to their needs

**Material UI Core Components:**
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
  - Material Icons
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



**Your report will need to describe the system's approach to testing and configuration. How is automated testing integrated into the code (if at all)? What infrastructure or architecture is needed to enable this testing? Considering how you would "run the tests" and what that would do is a good place to start. Similarly, is there any particular configuration work needed when building or using this system (including e.g., use of particular git branches or tags/labeling)?**

Material UI has many different tests including unit tests, integration tests, end to end (e2e) tests, and visual regression tests. The test folder in root contains e2e tests and visual regression tests while the package folder contains a unit and integration test for each component. For testing, MUI uses tools like @testing-library/react, chai, sinon, mocha, karma, playwright, jsdom, and enzyme. Automated testing is integrated in its visual regression tests where they use playwright to iterate over fixtures and take a screenshot. Each fixture can be described as a rendered UI. This tests the rendering of React components. End to end testing also utilizes playwright and is similar to the visual regression tests where it looks at a single fixture. Focusing on building this system, to add a unit test or integration test, run `yarn t TheUnitInQuestion`, implement the tested behavior, then open a PR  once the test passes. A particular configuration work when adding to this system is that you need to follow. Starting with forking then cloning the repo, then the contributor needs to create a new topic branch, then make a Pull Request (PR). Details here: https://github.com/mui/material-ui/blob/master/CONTRIBUTING.md  To install the mui package, you can do `npm install @mui/material @emotion/react @emotion/styled`.  To run tests, use `yarn test:unit` or `yarn test:unit –grep ComponentName` for unit tests, `yarn docs:api` for checking code formats and lints the repo, `yarn test:karma` to run unit tests in multiple browsers via BrowserStack. To deploy, go to deploy/netlify to render a preview of the docs with your changes. `yarn docs:build` or `yarn docs:export1 usually fails locally. `codecov/project` monitors coverage of the tests.

## Applied Perspective

**Perform some of the activities mentioned to "apply the perspective". This will often involve analyzing, diagramming, documenting, or assessing some aspect of the system or perspective. The exact format of this section will depend on your specific and chosen activities. Note that an analysis activity can overlap with the discussion of a concern. Your report should include around 2 activities (depending on their size).**
* For example, from an Evolution perspective, you might "Characterize the Evolution Needs" and "Assess the Current Ease of Evolution".

1. Usability Evaluation: Conduct a usability evaluation of specific Material-UI components or the overall UI design. This can involve tasks such as heuristic evaluations, cognitive walkthroughs, or usability testing with representative users. The goal is to identify any usability issues, pain points, or areas for improvement in terms of user interaction, navigation, visual design, or responsiveness.

2. User Flow Analysis: Analyze the user flows and interactions within the Material-UI components used in your application. Identify the key user tasks, actions, and navigation patterns. Create user flow diagrams or storyboards to visualize the sequences of screens and interactions, evaluating the ease of use and clarity of the user journey.

## Identify Styles & Patterns Used

**Software Design Patterns: Your will identify 4 or more design patterns (e.g., OOP Patterns) that are are used in the implementation of your system. (You should find at least 3 different patterns—a single pattern used in 2 different places can both be counted in the required 4). Your report will need to name each pattern being used, then provide an explanation of how the system uses that pattern. Don't just say where the pattern is; explain how this particularly implementation fits the requirements of the pattern. The goal is to demonstrate you understand the pattern's structure and usage.**

 Decorator Pattern - involves dynamically adding behaviors or responsibilities to an object by wrapping it with another object of the same interface.
 In Material-UI, High order components or HOCs are used to inject certain features or behaviors into components, such as handling theming, managing state, or providing access to certain context or data. These HOCs can be applied to existing components to extend their capabilities without modifying their underlying implementation. This promotes code reusability and modularity by separating concerns and allowing components to be composed with different functionalities. While the concept of enhancing components through HOCs shares some similarities with the Decorator Pattern, it is important to note that the implementation in Material-UI may not strictly adhere to the full structure and principles of the Decorator Pattern.


## Architectural Assessment

Open/Close Principle (OCP) - Material-UI adheres to the Open/Closed Principle by providing an extensible framework of reusable components that can be customized and extended through props. Instead of modifying the internal implementation, developers can leverage props to tailor the appearance, behavior, and functionality of components to fit their specific requirements. This approach promotes code reusability, maintainability, and modularity, allowing for the addition of new features without modifying the existing codebase.

## System Improvement


## Footnotes
[^1]: Component API available at: https://mui.com/

[^2]: Documentation on packages: https://mui.com/material-ui/guides/understand-mui-packages/

[^3]: Core packages offered by Material UI: https://mui.com/blog/mui-product-comparison/

[^4]: Material UI github packages: https://github.com/mui/material-ui/tree/master/packages
