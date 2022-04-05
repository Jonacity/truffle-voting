# Voting Project Tests

## Install dependencies

```
npm install

// Install truffle
npm install truffle

// Install ganache
npm install ganache-cli

// Install eth-gas-reporter
npm install eth-gas-reporter
```

## Run unit tests

```
// Run ganache
ganache-cli

// Run migrations
truffle migrate

// Run tests
truffle test
```

> 28 passing tests

*All the contract functions are tested.*

1 file: `VotingTest.js`

### 1) Add voters

- Should **start** at first workflow status ✔
- Should **add** voters ✔
- Should **emit** an event adding a voter ✔
- Should **revert** adding a voter already registered ✔
- Should **revert** adding a voter from a voter ✔

### 2) Get a voter

- Should **get** a voter ✔
- Should **revert** getting a voter from unregistered address ✔

### 3) Add proposals

- Should **revert** adding proposal before proposal registration ✔
- Should **add** a proposal ✔
- Should **add** another proposal from the same user ✔
- Should **emit** an event adding a proposal ✔
- Should **revert** adding proposal without description ✔
- Should **revert** adding proposal from unregistered address ✔

### 4) Get a proposal

- Should **get** a proposal ✔
- Should **revert** getting proposal from unregistered address ✔

### 5) Set vote

- Should **revert** voting before voting session started ✔
- Should **emit** an event starting the voting session ✔
- Should **emit** an event after a vote ✔
- Should **revert** voting twice ✔
- Should **increment** voteCount on a proposal ✔
- Should **revert** voting for invalid proposal id ✔
- Should **revert** voting when proposal id equals to proposalsArray length ✔
- Should **update** voted proposal id after voting ✔
- Should **revert** voting from unregistered address ✔

### 6) Tally votes

- Should **revert** tally votes before voting session ended ✔
- Should **tally** votes ✔
- Should **emit** an event after tally votes ✔
- Should **revert** tallying votes from a voter ✔