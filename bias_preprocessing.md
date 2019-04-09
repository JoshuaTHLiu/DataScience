# Optimized Pre-Processing for Discrimination Prevention

 - Bias prevention can be addressed at multiple levels:
   - data (pre-processing)
   - model (in-processing)
   - prediction (post-processing)
 - Disparate impact can be detected with statistical parity and group fairness.
 - Individual fairness says that similar individuals are treated equally regardless of their group membership.

## PRE-PROCESSING TRANSFORMATION
 - aims to balance utility, discrimination prevention, and individual distortion
   - utility:
     - p(x,y) = p(x',y')

## TERMS
 - protected attributes - features that identify a group
 - disparate treatment - direct discrimination from using protected attributes
 - disparate impact - indirect discrimination from using attributes highly correlated with protected attributes
