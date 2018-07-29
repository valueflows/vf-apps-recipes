# vf-apps-recipes

People create recipes when they want to do the same thing in the same way repeatedly. Recipes go by a variety of different names in different domains and use several different models. Recipes are important for [Planning](https://github.com/valueflows/vf-apps-planning).

Recipe names:
* [Workflow model or definition](https://en.wikipedia.org/wiki/Workflow) used in several domains.
* [Bills of Material and Routings](https://www.managementstudyguide.com/production-module-bom-and-routing.htm) used mostly in manufacturing.
* The name Recipe is used mostly in cooking and food processing. We use that name here because we think it is used and understood by the most people.

Recipe models: a recipe consists of a series, tree, or graph of activities that may be called processes, operations, tasks, or similar words that generally describe transforming some inputs to create some outputs. In VF, we call those Processes. There are two main models for sequencing processes in recipe models:
* direct dependencies between processes, where one process is directly linked to its preceding and next processes.
* [input-process-output models](https://en.wikipedia.org/wiki/IPO_model), where one process is linked to others when one of its outputs becomes the input to another process, or vice versa.

ValueFlow uses an input-process-output model, not direct process dependencies. Here is [an explanation of some of the advantages of an IPO model](https://github.com/FreedomCoop/valuenetwork/wiki/Loose-coupling-vs-tight-coupling,-or,-direct-process-dependencies-vs-resource-flows).

Manufacturing systems until the 1990's used separate bills of material and routings, and the routings were a linear, numbered list of processes. An IPO model merges them into one chain, tree or graph. It is possible to transform a BOM+routing model to an IPO model and vice-versa for interoperation, if necessary. This is particularly accurate if the BOM+routing model uses a "routed bill" where each BOM component specifies which routing step it goes into.

The Recipe model in ValueFlows has not yet been specified and agreed upon. This repo will discuss possibilities in this issue: https://github.com/valueflows/vf-apps-recipes/issues/1.

Here are some example implementations of recipes:
* [From NRP](https://speakerdeck.com/mikorizal/5-nrp-recipe-concepts-and-tutorial) - also used in all of its forks.
* GOSH (Gathering for Open Science Hardware) has standardized on [DocuBricks](http://www.docubricks.com/).
* [Common Workflow Language](https://www.commonwl.org/) has specs and running software.
