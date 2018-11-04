# Architecture

## Project structure

### Goal

Follow best practice convension to get mantainable and scalable project

### HowTo

- how ngModules works
- core
- shared
- feature
- models
- barrels
- namming
- automation
- tsconfig.paths

### Links

- [Avoiding common confusions with modules in Angular](https://blog.angularindepth.com/avoiding-common-confusions-with-modules-in-angular-ada070e6891f)
- [Structure example](https://github.com/viovendi/viovendi-web/blob/master/app/core/index.ts)
- [12 Things to Help Large Organizations Do Angular Right](https://blog.nrwl.io/12-things-to-help-large-organizations-do-angular-right-f261a798ad6b)
- [Nrwl/nx](https://nrwl.io/nx)
- [Organize Ng app](https://medium.com/@michelestieven/organizing-angular-applications-f0510761d65a)
- [How to use paths in tsconfig.json](https://stackoverflow.com/questions/43281741/how-to-use-paths-in-tsconfig-json)
- [tsconfig-paths](https://www.npmjs.com/package/tsconfig-paths)

## Code structure

### Goal

Set up consistance codding rules. Only automation correction really work

### HowTo

- Barrels
- Prettier
- Imports, class members, constructor injectors with tslint + eslint-rules + codelyzer
- Follow ng-styleguide
- npm tasks with --fix

### Links

- [Barrels](https://basarat.gitbooks.io/typescript/docs/tips/barrel.html)
- [circular-dependency-plugin](https://github.com/aackerman/circular-dependency-plugin)
- Tslint rules
  - [tslint:recommended](https://github.com/viovendi/viovendi-web/blob/develop/tslint.json#L3)
  - [codelyzer](https://github.com/mgechev/codelyzer)
  - [ordered-imports](https://palantir.github.io/tslint/rules/ordered-imports/)
  - [lines-between-class-members](https://eslint.org/docs/rules/lines-between-class-members)
  - [newline-after-var](https://eslint.org/docs/rules/newline-after-var)
  - [no-inferrable-types](https://palantir.github.io/tslint/rules/no-inferrable-types/)
  - [typedef](https://palantir.github.io/tslint/rules/typedef/)

## Sharing codebase

### Goal

Main concepts to share reusable units

### HowTo

- npm-package
- monorepos
- microservices
- angular-elements/web-components

### Links

- npm-package
  - [pros/cons](https://speakerdeck.com/manfredsteyer/architecture-for-huge-enterprise-applications-npm-packages-monorepos-and-micro-apps?slide=17)
  - [ng-packagr](https://github.com/ng-packagr/ng-packagr)
  - [Creating a Library with the Angular CLI](https://blog.angularindepth.com/creating-a-library-in-angular-6-87799552e7e5)
- monorepos
  - [pros](https://speakerdeck.com/manfredsteyer/architecture-for-huge-enterprise-applications-npm-packages-monorepos-and-micro-apps?slide=20)
  - [cons](https://speakerdeck.com/manfredsteyer/architecture-for-huge-enterprise-applications-npm-packages-monorepos-and-micro-apps?slide=27)
  - [Why Google Stores Billions of Lines of Code in a Single Repository](https://ai.google/research/pubs/pub45424)
  - [Monorepos in the wild](https://medium.com/@maoberlehner/monorepos-in-the-wild-33c6eb246cb9)
  - [Monorepos By Example](https://codeburst.io/monorepos-by-example-part-1-3a883b49047e)
  - [awesome-monorepo](https://github.com/korfuri/awesome-monorepo)
- microservices
  - [example1](https://speakerdeck.com/manfredsteyer/architecture-for-huge-enterprise-applications-npm-packages-monorepos-and-micro-apps?slide=36)
  - [example2](https://speakerdeck.com/manfredsteyer/architecture-for-huge-enterprise-applications-npm-packages-monorepos-and-micro-apps?slide=37)
  - [pros/cons](https://speakerdeck.com/manfredsteyer/architecture-for-huge-enterprise-applications-npm-packages-monorepos-and-micro-apps?slide=33)
- angular-elements/web-components
  - [distribute guide](https://medium.com/codingthesmartway-com-blog/angular-elements-a-practical-introduction-to-web-components-with-angular-6-52c0b3076c2c)
  - [Mastering Web Components with stencil](https://ionicthemes.com/tutorials/about/ionic-4-tutorial-mastering-web-components-in-ionic-4)

## Build and distribute the app

### Goal

Achive prefererable local and production experience

### HowTo

- Consistance build with ng-cli if it's possible, extends with builders
- Up to date versioning
- Custom build with webpack4 + @ngtools/webpack + AngularCompilerPlugin + node v10+
- Rollup plan
- Tech expert + delivery phase

### Links

- AOT
  - [Follow AOT rules](https://medium.com/spektrakel-blog/angular-writing-aot-friendly-applications-7b64c8afbe3f)
  - [Multiple entry points as sequential pipeline](https://github.com/angular/devkit/issues/861#issuecomment-391797538)
  - [Dynamic html with AOT](https://github.com/viovendi/viovendi-web/blob/ea20973f7005fc43aedf8dbb16ccb563de0f29b5/app/manager/components/campaign/shared/components/dynamic-template/dynamic-template.component.ts)
  - [Provide JIT compiler](https://github.com/viovendi/viovendi-web/blob/0ea9cf0f539356fcbd08fb80d817498e3bbda129/app/manager/components/campaign/core/core.module.ts)
  - [Issue](https://github.com/angular/angular/issues/20875#issuecomment-352116929)
  - [One more](https://blog.angularindepth.com/here-is-what-you-need-to-know-about-dynamic-components-in-angular-ac1e96167f9e#1b56)
- ng eject in CLI v6+
  - [Angular CLI 6 under the hood — builders demystified](https://medium.com/dailyjs/angular-cli-6-under-the-hood-builders-demystified-f0690ebcf01)
  - [Custom webpack builders for Angular build facade](https://github.com/meltedspark/angular-builders/tree/master/packages/custom-webpack)
- [Bazel](https://github.com/jin/awesome-bazel)

# SCV

### Goal

Follow git rulles

### HowTo

- Branch flow
- master restriction
- Code owners
- PRs are responsibility of the whole team
- Labels + Milestones, tags if needed
- Liner history if needed
- Test coverage + unit test pluggins
- Hooks
- Slack bot

### Links

- [About pull request merges](https://help.github.com/articles/about-pull-request-merges/)
- [Why you should stop using rebase](https://medium.com/@fredrikmorken/why-you-should-stop-using-git-rebase-5552bee4fed1)
- [10 Principles of a Good Code Review](https://dev.to/codemouse92/10-principles-of-a-good-code-review-2eg)
- [Best practices for pull requests](https://github.community/t5/Support-Protips/Best-practices-for-pull-requests/ba-p/4104)
- [Git hooks with husky](https://github.com/typicode/husky)

# Framework

## Debugging

### Goal

Debbug ng-app and observables

### HowTo

- From ts to debbuger
- From console.log to ng.probe
- Logging observales flow

### Links

- [Seven methods for debbuging ng app](https://angularfirebase.com/lessons/methods-for-debugging-an-angular-application)
- [Debugging Rxjs with rxjs-spy](https://blog.angularindepth.com/debugging-rxjs-4f0340286dd3)

## State management

### Goal

Define the problem and pick the right tool

### HowTo

- types of state
- state synchronization
- you should to know Redux
- investigate time into state structure: actions -> states -> reducers
- rule 1: separate state management from the rest of app
- rule 2: optimistic updates with error handling
- rule 3: immutable data
- rule 4: thing about achieving a ### goal, is not to use Redux
- rule 5: always treat Router as the source of truth
- ngrx/store / ngxs / akita / mobx
- guards as resolvers

### Links

- [Managing state in ng app](https://blog.nrwl.io/managing-state-in-angular-applications-22b75ef5625f)
- [Why another state management framework for Angular?](https://medium.com/@amcdnl/why-another-state-management-framework-for-angular-b4b4c19ef664)
- [Akita](https://netbasal.com/introducing-akita-a-new-state-management-pattern-for-angular-applications-f2f0fab5a8)
- [Guard example](https://github.com/viovendi/viovendi-web/blob/2528b1b2fc826f5868f6b5924a8b4d071e5b4ba7/app/manager/components/event/components/promo-code/core/guards/promo-codes/promo-codes.guard.ts#L21)

## Change detection

### Goal

Know how the magic works

### HowTo

- what and why ngzone?
- why CD is not triggered?
- how to trigger CD manually
- control your zone
- Expression has changed after it was checked error
- Pipes vs function call

### Links

- [I reverse-engineered Zones (zone.js) and here is what I’ve found](https://blog.angularindepth.com/i-reverse-engineered-zones-zone-js-and-here-is-what-ive-found-1f48dc87659b)
- [These 5 articles will make you an Angular Change Detection expert](https://blog.angularindepth.com/these-5-articles-will-make-you-an-angular-change-detection-expert-ed530d28930)
- [Triggering change detection manually in Angular](https://stackoverflow.com/questions/34827334/triggering-change-detection-manually-in-angular)
- [Everything you need to know about the ExpressionChangedAfterItHasBeenCheckedError error](https://blog.angularindepth.com/everything-you-need-to-know-about-the-expressionchangedafterithasbeencheckederror-error-e3fd9ce7dbb4)
- [Increasing Performance - more than a pipe dream](https://www.youtube.com/watch?v=I6ZvpdRM1eQ)

## DI

### Goal

Reveal how IoC is implemented

### HowTo

- what problem IOC does it solve?
- vanilla IOC in TS, inversifyJS
- provideIn vs providers[]
- InjectionToken, useClass, useFactory, useValue, NgModule.forRoot, forwardRef
- Keep constructors simple

### Links

- [Dependency Injection in TypeScript](https://nehalist.io/dependency-injection-in-typescript/)
- [Official guide](https://angular.io/guide/dependency-injection)
- [What is `forwardRef` in Angular and why we need it](https://blog.angularindepth.com/what-is-forwardref-in-angular-and-why-we-need-it-6ecefb417d48)

## Routing

TODO

# Unit testing

### Goal

Someday it may save our asses, or not

### HowTo

- place in the project
- structure of the spec
- Increase performance with Jest
- BDD is your friend, write test for your team
- Test coverage
- Git prepush hooks
- Github + CI

### Links

- [UT project guide](https://viovendi.atlassian.net/wiki/spaces/ENG/pages/416415905/Unit+testing+guide)
- [Scripts](https://github.com/viovendi/viovendi-web/blob/b215f3176ff2a5e72d6bc5ef729d56ea058eec98/package.json#L34)
  TODO
