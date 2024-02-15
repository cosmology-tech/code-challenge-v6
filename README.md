# UI and State Challenge

## Overview

In this challenge, you are tasked with creating a basic UI that enables users to add tokens to an asset list. Your application will feature a ComboBox for selecting assets and an "Add Asset" button to trigger the selection process. This challenge is designed to assess your skills in React component integration and state management.

## Challenge Steps

### Step 1: Project Setup

- Install `create-cosmos-app` globally using npm:

```bash
npm install -g create-cosmos-app
```

- Scaffold your project with the `connect-chain` template:

```bash
cca --template connect-chain
```

- Make sure to commit the boilerplate state in git as the first commit so we can see the commits more cleanly, BEFORE you make changes.

```bash
git init .
git add .
git commit -am "first commit"
```

### Step 2: State Management

- Add a state management library of your choice (e.g., Zustand, MobX).

### Step 3: Add Store

- Create a store that can `addAssetList`. Use `Chain` and `AssetList` types from the `@chain-registry/types`, and data from `chain-registry` — add a small set, 2-5 random assets from `chain-registry`. Choose a default chain, such as `"osmosis"`, and store it as something like `state.selectedChain`.

### Step 4: Build the UI

- Integrate and render the asset-list component as shown [here](https://cosmology.zone/explorer?category=asset&element=asset-list) and in the [storybook](https://storybook.cosmology.zone/?path=/docs/asset-assetlist--docs) — which should display the assets from the state.
- Implement an "Add Asset" button that, when clicked, opens a modal or another UI element of your choice.
- The modal (or popover or other) should render the ComboBox component, allowing the user to select an asset to add. Reference for the ComboBox implementation can be found in the [Cosmology Storybook](https://storybook.cosmology.zone/?path=/story/combobox--custom-combobox-item).
- The `state.selectedChain`, e.g., `osmosis` should determine which set of assets can show up in the list of assets.
- Upon selecting an asset from the ComboBox, the asset list should update to include the chosen asset. Likely should have a submit button to confirm.

### Step 5 (optional): Add the chain selector

- Integrate and render a chain selector using the `chain-registry`'s `Chain` infos.
- The modal (or popover or other) should render the ComboBox component, allowing the user to select a chain. Reference for the ComboBox implementation can be found in the [Cosmology Storybook](https://storybook.cosmology.zone/?path=/story/combobox--custom-combobox-item).
- The selected chain, e.g., `osmosis` should determine which set of assets can show up in the list of assets.
- Upon selecting a chain from the ComboBox, it will change the `state.selectedChain`


## Requirements

- No real data handling like deposit/withdraw actions is required.
- No need to connect a wallet or implement authentication.
- Focus on UI implementation and state management.

## Bonus

Not required, but if that was simple for you, consider adding the following as a bonus:

- A layout, a menu, or some organization

## Submission Guidelines

- DO NOT fork this repo.
- When you clone the repo, make sure to commit the boilerplate state so we can see the commits more cleanly.
- Ensure your project is available on GitHub or a similar platform.
- Include a README in your repository with instructions on how to run your project.

Good luck!
