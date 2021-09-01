# sst-triage-ts-jest

1. Yarn install at the root
```
yarn
```

2. Go into the SST app
```
cd packages/serviceA
```

3. Run tests
```
yarn test
```

The output is
```
$ sst test
Preparing your SST app
Detected tsconfig.json
Transpiling source
Linting source
Running type checker
 PASS  test/MyStack.test.ts (13.865 s)
  ✓ Test Stack (6650 ms)

  console.log
    Building Lambda function src/lambda.handler

      at Object.builder (../../node_modules/@serverless-stack/resources/src/util/nodeBuilder.ts:131:11)
          at Array.forEach (<anonymous>)

  console.log
    Linting Lambda function source

      at App.runLint (../../node_modules/@serverless-stack/resources/src/App.ts:372:13)
          at Array.forEach (<anonymous>)

  console.log
    Type checking Lambda function source

      at App.runTypeCheck (../../node_modules/@serverless-stack/resources/src/App.ts:409:13)
          at Array.forEach (<anonymous>)

Test Suites: 1 passed, 1 total
Tests:       1 passed, 1 total
Snapshots:   0 total
Time:        14.933 s
Ran all test suites.
✨  Done in 24.68s.
```
