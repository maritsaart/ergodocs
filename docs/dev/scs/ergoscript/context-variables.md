# Utilizing Context Variables in ErgoScript

ErgoScript allows for more complex programs with predicates defined on context. Consider the following example:

```scala
HEIGHT < 4000000            // address 2fp75qcgMrTNR2vuLhiJYQt
```

This script uses the context variable `HEIGHT`, which signifies the height of the block in which the transaction is mined. If the blockchain height is less than 4,000,000, the box associated with this address becomes "anyone-can-spend". Conversely, if the blockchain height equals or exceeds 4,000,000, the box becomes "no-one-can-spend".

Apart from `HEIGHT`, ErgoScript supports other context variables such as `OUTPUTS`, `INPUTS`, and `minerPubKey`. These variables offer additional tools for writing more specific and flexible scripts. For more details on context variables and their usage, please refer to the [official documentation](https://github.com/ScorexFoundation/sigmastate-interpreter/blob/develop/docs/LangSpec.md).