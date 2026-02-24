# Questions
- Some common steps in a CI setup include linting, testing, and building. What are the specific tools for taking care of these steps in the ecosystem of the language you picked? You can search for the answers by Google.
- What alternatives are there to set up the CI besides Jenkins and GitHub Actions? Again, you can ask Google!
- Would this setup be better in a self-hosted or a cloud-based environment? Why? What information would you need to make that decision?

# Answers
## CI Tools
I choose .NET/C#. For linting you can use any of the popular IDEs, like Visual Studio or JetBrains Rider. You can also use a .editorconfig file, this works in a similar way as the eslint config file. For testing you can use one of many frameworks, like xUnit, NUnit and MSTest. Building is done either through your IDE or through MSBuild the `dotnet build` cli command.

## Alternatives
The are many alternatives for CI/CD. The 3 largest cloud providers, Amazon, Google and Microsoft all provide the ability to apply CI/CD on your project on their cloud. 

Other notable alternatives according to AlternativeTo:
  - Travis CI
  - Cicada.sh
  - CircleCI
  - GitLab CI/CD

## Self-hosted vs cloud
Choosing between a self-hosted or cloud based could depend on factors like:
  - Time & Cost
  - In-house knowledge
  - Project requirements, e.g. privacy/safety

Basically if I were to chose I would first look at what infrastructure I have available, how big is my budget, and am I (or someone else in my company) able to maintain the self-hosted infrastructure. Then I would take into account project based constraints. Let's say the application would work with data from EU citizens. Would the cloud solution comply with GDPR? Is the data stored outside the EU? And other similar juridical questions.
