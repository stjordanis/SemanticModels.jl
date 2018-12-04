# SemanticModels.jl

computational representations of model semantics with knowledge graphs for
metamodel reasoning.

## Goals

1. Extract a knowledge graph from Scientific Artifacts (code, papers, datasets)
2. Represent scientific models in a high level way, (code as data)
3. Build metamodels by combining models in hierarchical expressions using reasoning over KG (1).

## Running Example: Influenza

Modeling the cost of treating a flu season taking into account weather effects.

1. Seasonal temperature is a dynamical system
2. Flu infectiousness γ is a function of temperature

## Running Example: Modeling types

Modeling the cost of treating a flu season taking into account weather effects.

1. Seasonal temperature is approximated by 2nd order linear ODE
2. Flu cases is an SIR model 1st oder nonlinear ode
3. Mitigation cost is Linear Regression on vaccines and cases

## Scientific Domain

We focus on Susceptible Infected Recovered model of epidemiology.

1. Precise, concise mathematical formulation
2. Diverse class of models, ODE vs Agent based, determinstic vs stochastic
3. FOSS implementations are available in all three Scientific programming languages

## Knowledge Extraction Architecture

![Knowledge Extraction Architecture](img/extraction.dot.svg)

## Example Input Packages

1. EMOD, Epimodels, NetLogo, and FRED are established packages, given their maturity and availability of published
papers citing these packages. 
2. Pathogen and NDLib are newer packages, we expect easier to work with and more future adoption.
3. Textbooks [@voit_first_2012] and lecture notes[^1] will be a
resource for these simple models that are well characterized.

## Knowledge Graph

Picture of KG sample

![Hypothetical Knowledge Graph Sample](img/knowledgegraph.dot.svg)

## Knowledge Graph Schema

A preliminary design for types of knowledge in our knowledge graph.
![Knowledge Graph Schema](img/schema.dot.svg)

## Flu Metamodel Pipeline

Here is the DAG for our running example.
![A pipeline for modeling flu vaccination requirements](img/flu_pipeline.dot.svg)

See [FluModel](@ref) for worked out example.

## Infectious Disease Metamodel

- A more ambitious example of a metamodel
- Requires Agent based simulations of information diffuision and disease spread

![A DAG of model dependencies](img/metamodel.dot.svg)

## Static vs Dynamic Graph

- Inherent tradeoff between flexibility and static analysis
- We will build the computation graph through the execution of code
- Metaprogramming will be used to generate the executable codes

## Validation


## Conclusions

[^1]: <http://alun.math.ncsu.edu/wp-content/uploads/sites/2/2017/01/epidemic_notes.pdf>