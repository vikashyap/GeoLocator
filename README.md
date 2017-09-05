# React
A Geo Locatior app created in React
# 1. React
## The following features are supported:

```Functional Component

const App = () => (
    <div className='main-app'>
        <h1>Hello, World!</h1>
    </div>
);
Class Component

class App extends Component {
    render() {
        return (
            <div className='main-app'>
                <h1>Hello, World!</h1>
            </div>
        );
    }
}
Class Properties

class Menu extends Component {
    static propTypes = {
        className: PropTypes.string,
    };
    ...
}
Export Default

export default App;
Import .scss in Component

import './styles.scss';
const App = () => <div />;
```
## 2. Localization
We use Yahoo's React Intl (v2.0) library to support localization.

## 1. To support a new locale, e.g. ja-JP, copy i18n/en-US.properties to i18n/ja-JP.properties, translate the locale messages.

## 2. Specify a LOCALE env var in npm start to debug for a specific locale:

`$ LOCALE=en-US npm start
You can also build the bundle.js for a specific locale:

$ LOCALE=en-US npm run build
This will output the English bundle.js in dist/en-US folder. Note, if you don't specify LOCALE, default is en-US.`

## 3. To build bundle.js for all languages:

`$ npm run release
This will output each supported language bundle.js along with the style sheets in dist/{locale} folder.`

## 3. Webpack dev server
`When you run your project by npm start, webpack dev server watches the source files for changes and when changes are made the bundle will be recompiled.`

## 4. Sass loader
`You can define styles for individual React components using import. The good thing about importing styles is that you can define some base styles and import them for component-level styles.`

## 5. Unit test
```Assert & Expect

import { assert, expect } from 'chai';
...
Enzyme

import { shallow } from 'enzyme';
describe('Testing', () => {
    it('should render the App', () => {
        const wrapper = shallow(<App />);
        ...
    });
});
Sinon

const sandbox = sinon.sandbox.create();
describe('Testing', () => {
    afterEach(() => sandbox.verifyAndRestore());
    it('should call the callback', () => {
        const callback = sandbox.stub();
        ...
    });
});```
## 6. Coverage Report
```Code coverage report is geneated by istanbul. npm run coveralls will submit the coverage report to coveralls.io.

You can setup passing thresholds for statements, branches, functions and lines.

Example:

==================== Coverage / Threshold summary =============================
Statements   : 100% ( 46/46 ) Threshold : 90%, 4 ignored
Branches     : 100% ( 31/31 ) Threshold : 90%, 13 ignored
Functions    : 100% ( 10/10 ) Threshold : 90%
Lines        : 100% (  6/6  ) Threshold : 90%
================================================================================
The HTML and lcov reports can be found in the coverage folder.
```

# What can you do in the scaffolded project

## 1. Run the project
Launch webpack dev server

`$ npm start
then navigate to http://localhost:5000 in your browser.`

## 2. Lint js and scss source codes
ESLint with React linting options have been enabled.

`$ npm run lint`
## 3. Unit test
Start Karma test runner.

`$ npm run test`
Coverage report will be generated.

## 4. Build the bundle
Build files for production

`$ npm run build`
##5. Clean workspace
Remove dist and coverage folders

`$ npm run clean`
## For localization feature
1. Hot-load for a lanuage
$ LOCALE=en-US npm start
2. Build bundle.js for a language
$ LOCALE=en-US npm run build
3. Build all language bundles
$ npm run release
