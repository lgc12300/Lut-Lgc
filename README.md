
Latin Hypercube Sampling (LHS) combined with the Partial Rank Correlation Coefficient (PRCC) is a statistical technique used for sensitivity analysis, which assesses how changes in model input variables affect the output. The PRCC method is highly effective for models with a monotonic relationship between inputs and outputs, meaning that as an input increases or decreases, the output consistently moves in the same direction (either upward or downward), a characteristic of monotonic behavior. PRCC is particularly suitable for evaluating the strength and direction of these monotonic relationships in non-linear models. However, it is not ideal for non-monotonic models, where the relationship between inputs and outputs may reverse direction.

Thus, PRCC, when paired with Latin Hypercube Sampling (LHS), serves as an efficient method for sensitivity analysis in models with monotonic input-output relationships. This approach is especially valuable for non-linear models, where traditional linear sensitivity analysis methods may fail to provide reliable results. In comparison, methods such as EFAST and Sobol are better suited for capturing both linear and non-linear relationships, including non-monotonic interactions, by exploring the model's behavior across its full parameter space.

To perform the PRCC analysis, update your model and parameters in silihs_ode_lhs.m and param_settings_lhs.m, respectively, and then run the following MATLAB scripts in sequence:

model_lhs.m
run_prcc.m
plot_prcc.m
