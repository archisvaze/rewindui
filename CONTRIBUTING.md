## Contributing guidelines
Thank you for considering contributing to this project! We appreciate your time and effort in making this project better.

## Tech stack
Rewind-UI is built as a [monorepo using Turborepo](https://turbo.build/repo/docs/handbook/what-is-a-monorepo) on top of the following amazing projects:
- [React](https://reactjs.org/)
- [TailwindCSS](https://tailwindcss.com/)
- [CVA](https://cva.style)
- [Storybook](https://storybook.js.org/)
- [Next.js](https://nextjs.org/)
- [TypeScript](https://www.typescriptlang.org/)
- [Floating-UI](https://floating-ui.com/)

Basic animations are implemented using the [Web Animations API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Animations_API). For more complex animations we use [Framer Motion](https://www.framer.com/motion/).

Before you get started, please take a moment to review the following guidelines.

## Ways to contribute
There are many ways to contribute to this project! Here are some ideas:
- Submit bugs and feature requests
- Review source code changes
- Review the documentation and make pull requests for anything from typos to new content
- Review open issues
- Contribute to the codebase

## Submitting an issue
If you encounter a bug, have a feature request, or need assistance, please submit an issue using the issue tracker. Before submitting an issue, please check if a similar issue already exists. Include as much detail as possible to help us understand and address the problem.

## Contribution workflow
1. Fork the repository
2. Create a new branch for your changes
3. Make your changes
4. Commit your changes
5. Push your changes to your fork
6. Submit a pull request
7. Wait for your pull request to be reviewed
8. Make changes to your pull request if the reviewer requests them
9. Celebrate your success after your pull request is merged!

## Local development
After cloning the repository, you can run the following commands:

- [Install pnpm](https://pnpm.io/installation) globally: `npm install -g pnpm`
- Install repository dependencies: `pnpm install`

Having installed the dependencies, you need to start the dev servers for each package/app:

### @rewind-ui/core
Open the `rewindui/packages/core` directory and run `pnpm dev` to start the development server on the core package.

### Storybook
Open the `rewindui/apps/storybook` directory and run `pnpm dev` to start the Storybook server.
Storybook is used to develop and test components in isolation.

### Documentation
Open the `rewindui/apps/docs` directory and run `pnpm dev` to start the documentation server.

## Project structure
The structure of each component should be as follows:

### @rewind-ui/core
Each component should be in its own directory inside `rewindui/packages/core/src/components`. The [Button](https://github.com/rewindui/rewindui/tree/main/packages/core/src/components/Button) component can be used as an example.

The component directory should contain the following files:
- `index.ts` - exports the component and its types
- `Component.tsx` - contains the component logic
- `Component.types.ts` - contains the component types
- `Component.tests.tsx` - contains the component tests

The CVA file of each component should be placed in `rewindui/packages/core/src/theme/styles/Component.styles.ts` and should also be exported from `rewindui/packages/core/src/theme/styles/index.ts`. The `theme.context.tsx` file will need to be adjusted to include the new component.

Each component should be exported from `rewindui/packages/core/src/index.ts` as well.

### Storybook
To add a new component to Storybook, add a new story file in `rewindui/apps/storybook/stories` and import the component from `@rewind-ui/core`.

### Documentation
It is recommended to submit your pull request without documentation changes. If the new component is accepted, the documentation will be updated by the maintainers.
