## Formalization of the Church-Rosser Theorem in Arend


This project is a direct port and adaptation of an existing formalization written in **Agda**. 

The repository formalizes four distinct approaches to proving the theorem:
1) Tait/Martin-Löf Method: Uses the classic parallel reduction ($\beta^*$) and the diamond property.
2) Parallel Takahashi Method: Enhances the Tait/Martin-Löf proof using Takahashi’s complete developments' translation.
3) Komori/Matsuda/Yamakawa Method: Proves confluence for $\beta$-reduction directly via iterated Takahashi translation, bypassing parallel reduction entirely.
4) Dehornoy’s Z-property Method: Establishes confluence as a corollary of the abstract Z-property, reusing lemmas proven in the Komori method.

The theoretical framework, proofs structure, and de Bruijn index syntax definitions in this repository are based on the following work:

1. Original Agda Repository: [iwilare/church-rosser](https://github.com/iwilare/church-rosser)
2. B.Sc. Thesis: [Formalization of the Church-Rosser Theorem in Agda](https://iwilare.com/bsc-thesis.pdf) by iwilare.

## Project Structure

* `src/Syntax.ard` — Definitions of $\lambda$-terms using de Bruijn indices and substitution ($\sigma$-calculus) operations.
* `src/Beta.ard` — Definition and core properties of single-step $\beta$-reduction and many-step $\beta^*$-reduction.
* `src/Parallel.ard` — Properties of parallel reduction.
* `src/Takahashi.ard` — Implementation of the Takahashi translation function.
* `src/ConfluenceParallel.ard` — Tait/Martin-Löf confluence proof.
* `src/ConfluenceParallelTakahashi.ard` — Takahashi-optimized parallel reduction proof.
* `src/ConfluenceTakahashi.ard` — Komori et al. confluence proof.
* `src/ConfluenceZ.ard` — Confluence proof based on Dehornoy's Z-property.

