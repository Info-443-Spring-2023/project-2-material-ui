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


**Development View**

**Your report will need to describe the system's approach to testing and configuration. How is automated testing integrated into the code (if at all)? What infrastructure or architecture is needed to enable this testing? Considering how you would "run the tests" and what that would do is a good place to start. Similarly, is there any particular configuration work needed when building or using this system (including e.g., use of particular git branches or tags/labeling)?**
Material UI has many different tests including unit tests, integration tests, end to end (e2e) tests, and visual regression tests. The test folder in root contains e2e tests and visual regression tests while the package folder contains a unit and integration test for each component. For testing, MUI uses tools like @testing-library/react, chai, sinon, mocha, karma, playwright, jsdom, and enzyme. Automated testing is integrated in its visual regression tests where they use playwright to iterate over fixtures and take a screenshot. Each fixture can be described as a rendered UI. This tests the rendering of React components. End to end testing also utilizes playwright and is similar to the visual regression tests where it looks at a single fixture. Focusing on building this system, to add a unit test or integration test, run `yarn t TheUnitInQuestion`, implement the tested behavior, then open a PR  once the test passes. A particular configuration work when adding to this system is that you need to follow. Starting with forking then cloning the repo, then the contributor needs to create a new topic branch, then make a Pull Request (PR). Details here: https://github.com/mui/material-ui/blob/master/CONTRIBUTING.md  To install the mui package, you can do `npm install @mui/material @emotion/react @emotion/styled`.  To run tests, use `yarn test:unit` or `yarn test:unit –grep ComponentName` for unit tests, `yarn docs:api` for checking code formats and lints the repo, `yarn test:karma` to run unit tests in multiple browsers via BrowserStack. To deploy, go to deploy/netlify to render a preview of the docs with your changes. `yarn docs:build` or `yarn docs:export1 usually fails locally. `codecov/project` monitors coverage of the tests. 

**Applied Perspective**

**Perform some of the activities mentioned to "apply the perspective". This will often involve analyzing, diagramming, documenting, or assessing some aspect of the system or perspective. The exact format of this section will depend on your specific and chosen activities. Note that an analysis activity can overlap with the discussion of a concern. Your report should include around 2 activities (depending on their size).**
* For example, from an Evolution perspective, you might "Characterize the Evolution Needs" and "Assess the Current Ease of Evolution".

1. Usability Evaluation: Conduct a usability evaluation of specific Material-UI components or the overall UI design. This can involve tasks such as heuristic evaluations, cognitive walkthroughs, or usability testing with representative users. The goal is to identify any usability issues, pain points, or areas for improvement in terms of user interaction, navigation, visual design, or responsiveness.

2. User Flow Analysis: Analyze the user flows and interactions within the Material-UI components used in your application. Identify the key user tasks, actions, and navigation patterns. Create user flow diagrams or storyboards to visualize the sequences of screens and interactions, evaluating the ease of use and clarity of the user journey.

**Identify Styles & Patterns Used**

**Software Design Patterns: Your will identify 4 or more design patterns (e.g., OOP Patterns) that are are used in the implementation of your system. (You should find at least 3 different patterns—a single pattern used in 2 different places can both be counted in the required 4). Your report will need to name each pattern being used, then provide an explanation of how the system uses that pattern. Don't just say where the pattern is; explain how this particularly implementation fits the requirements of the pattern. The goal is to demonstrate you understand the pattern's structure and usage.**

 Decorator Pattern - involves dynamically adding behaviors or responsibilities to an object by wrapping it with another object of the same interface.
 In Material-UI, High order components or HOCs are used to inject certain features or behaviors into components, such as handling theming, managing state, or providing access to certain context or data. These HOCs can be applied to existing components to extend their capabilities without modifying their underlying implementation. This promotes code reusability and modularity by separating concerns and allowing components to be composed with different functionalities. While the concept of enhancing components through HOCs shares some similarities with the Decorator Pattern, it is important to note that the implementation in Material-UI may not strictly adhere to the full structure and principles of the Decorator Pattern.


**Achirtectural Assessment**
Open/Close Principle (OCP) - Material-UI adheres to the Open/Closed Principle by providing an extensible framework of reusable components that can be customized and extended through props. Instead of modifying the internal implementation, developers can leverage props to tailor the appearance, behavior, and functionality of components to fit their specific requirements. This approach promotes code reusability, maintainability, and modularity, allowing for the addition of new features without modifying the existing codebase.