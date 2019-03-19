# Aragon app with 0x dev-tools

This is a first attempt of using the new 0x tooling with Aragon stack. We start from the [react-kit boilerplate](https://github.com/aragon/aragon-react-kit-boilerplate).

## Before start

To better understand how this tools works this documentation is useful:

- [Web3 providers explained](https://0x.org/wiki#Web3-Provider-Explained)
- [sol-compailer](https://0x.org/docs/sol-compiler#introduction)
- [sol-trace](https://0x.org/docs/sol-trace)

Also There is a [truffle example](https://github.com/0xProject/dev-tools-truffle-example) made by the guys from 0x.

## Notes

0x tools needs to recompile our contracts cause they use a diferent format for their artifacts. They later use this to retrive infromation with `sol-trace` for example.

As a consecuense of the above to use truffle we need to configure a `TruffleArtifactAdapter`.

We need to use the web3 provider engine to compose a custom provider depending the mode we are using.
