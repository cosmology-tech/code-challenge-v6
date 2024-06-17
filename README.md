# UI and State Challenge

## Overview

In this challenge, you are tasked with creating a UI that enables users to add tokens to an asset list. Your application will feature a ComboBox for selecting assets and an "Add Asset" button to trigger the selection process, etc. This challenge is designed to assess your skills in React component integration and state management.

## Requirements

- Make sure to include all of the [deliverables](#deliverables) of your expertise.
  - If you're experienced in implementing UI components, you can focus on the [UI Components](#ui-components) part. And include state management and some of the business logic as a bonus.
  - Or you can focus on the [Business Logic](#business-logic) part, make the business logic readable and maintainable. For the UI, you can just make a rough one to show the data. And including a well implemented UI would be a bonus.
- No real data handling like deposit/withdraw actions is required.
- No need to connect a wallet or implement authentication.
- Focus on UI implementation and business logic.

## Setup

- You can use either vite or next app
- React
- Using Styled Components only (can use `emotion` or `styled-components`). Don't use any UI Kit.

## Deliverables

### UI Components

- [ ] Integrate and render the asset-list component as shown in the [storybook](https://storybook.cosmology.zone/?path=/docs/asset-assetlist--docs) — which should display the asset list.
- [ ] Implement an "Add Asset" button that, when clicked, opens a modal or another UI element of your choice.
- [ ] The modal (or popover or other) should render the ComboBox component, allowing the user to select an asset to add. Reference for the ComboBox implementation can be found in the [Cosmology Storybook](https://storybook.cosmology.zone/?path=/story/combobox--custom-combobox-item).
- [ ] The `state.selectedChain`, e.g., `osmosis` should determine which set of assets can show up in the list of assets.
- [ ] Upon selecting an asset from the ComboBox, the asset list should update to include the chosen asset. Likely should have a submit button to confirm.
- [ ] When the deposit button is clicked, open a modal as follows(Static component. No need to add functionalities):
![deposit](./deposit.png)
- [ ] Not required, but if that was simple for you, consider adding the following: A layout, a menu, or some organization

#### Notes

- Using `Styled Component` only. Don't use any UI Kit.
- `Theme` is optional.

### Business Logic

- [ ] Add a state management library of your choice (e.g., Zustand, MobX).
- [ ] Create a store that can `addAssetList`. Use `Chain` and `AssetList` types from the `@chain-registry/types`, and data from `chain-registry`
— [ ] Add a small set, 2-5 random assets from `chain-registry`. Choose a default chain, such as `"osmosis"`, and store it as something like `state.selectedChain`.
- [ ] Implement a configurable data source adapter to support multiple data sources. Implement two data source providers as follows, and then config to use one of these potential data sources when starting the demo:
  - chain-registry
  - @chain-registry/client

#### Notes

- DO NOT add any other dependencies unless there's a good reason. Use libs provided in the boilerplate only is preferred.
- Show your consideration on readability, maintainability and optimization.

## Submission Guidelines

- Include this README in your repository with checked [deliverables](#deliverables) and instructions on how to run your project.
- DO NOT fork this repo.
- Make sure to commit the boilerplate state in git as the first commit so we can see the commits more cleanly, BEFORE you make changes.
- Ensure your project is available on GitHub or a similar platform.

Good luck!
