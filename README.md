# sst-triage-ts-jest

1. Yarn install at the root
```
yarn
```

2. Run tests at the root, it should pick up 2 tests, 1 inside `test/` and 1 inside `packages/serviceA/`
```
yarn test
```

The output is
```
~/Sites/fwang/sst-triage-ts-jest$ yarn test
yarn run v1.22.10
$ sst test
Preparing your SST app
Detected tsconfig.json
Transpiling source
Linting source
Running type checker
 PASS  packages/serviceA/lambda.test.ts (7.16 s)
 PASS  test/MyStack.test.ts (17.133 s)
  ● Console

    console.log
      Building Lambda function packages/serviceA/lambda.handler

      at Object.builder (node_modules/@serverless-stack/resources/src/util/nodeBuilder.ts:131:11)
          at Array.forEach (<anonymous>)

    console.log
      Linting Lambda function source

      at App.runLint (node_modules/@serverless-stack/resources/src/App.ts:372:13)
          at Array.forEach (<anonymous>)

    console.log
      Type checking Lambda function source

      at App.runTypeCheck (node_modules/@serverless-stack/resources/src/App.ts:409:13)
          at Array.forEach (<anonymous>)


Test Suites: 2 passed, 2 total
Tests:       2 passed, 2 total
Snapshots:   0 total
Time:        18.431 s, estimated 20 s
Ran all test suites.
✨  Done in 30.31s.
```
