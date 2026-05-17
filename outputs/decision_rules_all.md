# Decision Rules from net_v2a

12 decision points trained on BPIC-17.

## `p_18`
- Branches (2): ['A_Incomplete', 'loop_18']
- Tree depth: 0, leaves: 1

```
|--- class: 1

```

## `p_14`
- Branches (2): ['A_Validating', 'loop_14']
- Tree depth: 1, leaves: 2

```
|--- OfferedAmount <= 19749.50
|   |--- class: 0
|--- OfferedAmount >  19749.50
|   |--- class: 0

```

## `p_3`
- Branches (2): ['A_Concept', 'loop_3']
- Tree depth: 0, leaves: 1

```
|--- class: 0

```

## `p_10`
- Branches (2): ['W_Call after offers', 'loop_10']
- Tree depth: 0, leaves: 1

```
|--- class: 0

```

## `p_21`
- Branches (2): ['A_Validating', 'loop_21']
- Tree depth: 0, leaves: 1

```
|--- class: 0

```

## `p_13`
- Branches (2): ['loop_13', 'W_Validate application']
- Tree depth: 3, leaves: 4

```
|--- OfferedAmount <= 2499.50
|   |--- class: 0
|--- OfferedAmount >  2499.50
|   |--- FirstWithdrawalAmount <= 16075.00
|   |   |--- class: 0
|   |--- FirstWithdrawalAmount >  16075.00
|   |   |--- FirstWithdrawalAmount <= 18975.00
|   |   |   |--- class: 1
|   |   |--- FirstWithdrawalAmount >  18975.00
|   |   |   |--- class: 0

```

## `p_11`
- Branches (2): ['loop_11', 'A_Complete']
- Tree depth: 0, leaves: 1

```
|--- class: 1

```

## `p_2`
- Branches (2): ['loop_2', 'W_Complete application']
- Tree depth: 0, leaves: 1

```
|--- class: 1

```

## `p_5`
- Branches (2): ['A_Accepted', 'loop_5']
- Tree depth: 1, leaves: 2

```
|--- OfferedAmount <= 8249.50
|   |--- class: 1
|--- OfferedAmount >  8249.50
|   |--- class: 0

```

## `p_17`
- Branches (2): ['W_Call incomplete files', 'loop_17']
- Tree depth: 0, leaves: 1

```
|--- class: 0

```

## `p_20`
- Branches (2): ['W_Validate application', 'loop_20']
- Tree depth: 5, leaves: 6

```
|--- OfferedAmount <= 30000.00
|   |--- MonthlyCost <= 289.19
|   |   |--- CreditScore <= 418.00
|   |   |   |--- MonthlyCost <= 182.86
|   |   |   |   |--- FirstWithdrawalAmount <= 3999.50
|   |   |   |   |   |--- class: 1
|   |   |   |   |--- FirstWithdrawalAmount >  3999.50
|   |   |   |   |   |--- class: 0
|   |   |   |--- MonthlyCost >  182.86
|   |   |   |   |--- class: 1
|   |   |--- CreditScore >  418.00
|   |   |   |--- class: 0
|   |--- MonthlyCost >  289.19
|   |   |--- class: 1
|--- OfferedAmount >  30000.00
|   |--- class: 0

```

## `p_23`
- Branches (2): ['O_Accepted', 'loop_23']
- Tree depth: 0, leaves: 1

```
|--- class: 0

```

