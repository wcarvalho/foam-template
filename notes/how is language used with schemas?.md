# Language + Schemas

Language describes the evolution of schema's over time. How does this help learning?

1. Language may be used to determine the latent code which is used for (a) reconstruction (b) the estimate of state at some moment (c) the description of some part of the environment to another agent?

``` mermaid
graph TD;
  t-->schema_1
  t+k-->schema_1
  schema_1-->language_1

  t+k+1-->schema_2
  t+k+n-->schema_2
  schema_2-->language_2

  language_1-->reconstruction
  language_2-->reconstruction

  language_1-->expression
  language_2-->expression
```
