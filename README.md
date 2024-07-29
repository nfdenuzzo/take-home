# Frontend Developer Assessment

DTN employs various assessments to determine if a candidate aligns with the role's expectations and the offered position.

This test aims to showcase your technical skills practically: you should deliver a solution that demonstrates a scalable front-end architecture, usability, and attention to requirement details.

## Instructions & Deliverables

This challenge will evaluate both your coding and communication skills. We value planning followed by execution, so please complete the SOLUTION.md.

1. Fork this repository to your GitHub account ([GitHub Help on Forking](https://help.github.com/articles/fork-a-repo/)).
2. Carefully read these instructions before starting the practical test.
3. Review the Requirements / Story Definition and Conditions of Acceptance.
4. Identify and document at least 3 test cases (no code required; Gherkin or a written list will suffice):
   - Show your understanding of the Conditions of Acceptance.
   - Identify relevant edge cases.
5. Develop a solution that highlights your skills and strengths.
   - Feel free to add, change, or modify any files in the project.
   - You may use Google or any other references.
6. Describe how you would build a better "Product" for this coding task in SOLUTION.md, including your estimates.
7. Once satisfied with your solution, submit a link to your forked repository.

## Additional Notes

- Although this test uses React, you can use any framework of your choice (e.g., Next.js, Vite with React).
- Demonstrate your approach to feature development and your skills.
- Time yourself to balance quality and delivery. There is no set deadline for this task, but you should estimate, complete, and measure your time. Please submit your estimate and actual time with your code solution.
- Ensure the solution is fully functional when we check out your code.
- Include any additional dependencies in package.json.
- Using third-party solutions is allowed, but ensure the majority of the code represents your work.
- Treat the API as if it were an external service, and utilize it correctly. Make sure you read the API documentation [here](./API_DOCS.md).

## Requirements / Story Definitions

### Technical Requirements

Develop an app where products are retrieved from the API and filters can be used to refine the results.

### Product Requirements

As a user, I want to list and filter products in a responsive table format with pagination.

```gherkin
  Scenario: Display products with pagination
    Given I visit the product collection page
    Then I expect to see a filters sidebar
    And I expect to see a table of products
    And I expect to see 10 products in the table
    And I expect to see pagination for the products

  Scenario: Filter products by tag "Petrol"
    Given I visit the product collection page
    Then I expect to see a filters sidebar for tags
    When I search for "Petrol" in the filters sidebar
    Then I expect to see 1 product in the resulting table

  Scenario: Filter products by price
    Given I visit the product collection page
    Then I expect to see a filters sidebar
    When I filter by "Price" "1.10" in the sidebar
    Then I expect to see 1 product in the resulting table

  Scenario: Filter products by contract and tag "Diesel"
    Given I visit the product collection page
    Then I expect to see a filters sidebar
    When I filter by "Contract" "Yes" in the sidebar
    And I search for "Diesel" in the filters sidebar
    Then I expect to see 1 product in the resulting table
```

### Additional Requirements

1. **Responsive Design**: The application should be responsive and work well on different screen sizes.
2. **Pagination**: Implement pagination with a maximum of 10 items per page.
3. **Third-Party Libraries**: You are allowed to use any third-party libraries to get the job done faster if applicable.
4. **Code Quality**: Ensure your code is clean, well-documented, and follows best practices.
5. **Commits**: Make regular commits with clear and concise messages. Demonstrate a logical progression of work.
6. **Maintainability**: Write code that is maintainable and easy to understand. Use modularization and separation of concerns.
7. **Simplicity**: Aim for simplicity in your solution. Avoid over-engineering.
8. **State Management**: If you do not use a state management library (e.g., Redux, MobX), explain which one you would use and why in the SOLUTION.md.

### Evaluation Criteria

Your submission will be evaluated based on the following criteria:

1. **Functionality**: Does the app work as expected? Are all the requirements met?
2. **Code Quality**: Is the code clean, well-organized, and easy to read?
3. **Commit History**: Are there frequent, meaningful commits that document the development process?
4. **Maintainability**: Is the code structured in a way that makes it easy to maintain and extend?
5. **Responsiveness**: Does the app work well on different devices and screen sizes?
6. **Use of Third-Party Libraries**: If applicable, how effectively are third-party libraries used to enhance the app?

## Getting Started with the React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

### Available Scripts

In the project directory, you can run:

#### `npm install`

Install all required packages for the project.

#### `npm start`

Runs the app in development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.\
You will also see any lint errors in the console.

#### `npm test`

Launches the test runner in interactive watch mode.\
See more information about [running tests](https://facebook.github.io/create-react-app/docs/running-tests).
