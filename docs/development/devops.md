# DevOps

At CAST we are exponents of the Agile methodology for software development. DevOps is a set of practices that came about as a result of this methodology. The need to continuously iterate through versions of a product means that processes should be in place to make repeated releases as pain-free as possible. The easier this process is, the less resistance there will be to experiment and take risks. The following practices have to the goal of creating an environment where releasing reliable applications, faster and more frequently, can occur.

## Continuous Integration (CI)

> Continuous Integration is a software development process
in which all development work is integrated at a predefined time
or event and the resulting work is automatically tested and built.
The idea is that development errors are identified very early in the process.

Setting up a CI server is the low hanging fruit when it comes to ensuring the quality of your releases. A CI server runs a pre-scheduled build of your system followed by running the test suite. The code is normally built and tested on every commit that is pushed to the `master` branch. This means that any breaking changes can be spotted as soon as possible.

#### Benefits of CI

* Bugs are detected as fast as possible. They are also easier to track down as breaking commit becomes obvious.
* Fixing bugs becomes much easier. They are spotted early, therefore the related code will still be fresh in your mind.
* If a bug emerges and the code needs to be reverted to a bug-free state not many changes will be lost.

## Deployment

Automating the deployment process brings huge benefits in our Agile world. As a general principle any process that can be automated, should be automated. This to reduce cognitive load on our brains and free up our energies for more creative tasks.

#### Benefits of Automated deployment

* More frequent releases due to decrease of errors in the deployment process.
* Anyone in a team can deploy the software. If only one person knows the deployment process then releases will be halted whenever they are away. Automated deployment means this knowledge is captured in the system, not in an individual's brain.
* More time can be spent coding, less on monotonous admin style tasks.

## References

* [Wikidedia on CI](https://en.wikipedia.org/wiki/Continuous_integration)
* [DWYL guide on setting up Travis](https://en.wikipedia.org/wiki/Continuous_integration)
