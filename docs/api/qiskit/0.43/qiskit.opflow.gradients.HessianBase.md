---
title: HessianBase
description: API reference for qiskit.opflow.gradients.HessianBase
in_page_toc_min_heading_level: 1
python_api_type: class
python_api_name: qiskit.opflow.gradients.HessianBase
---

# HessianBase

<span id="qiskit.opflow.gradients.HessianBase" />

`HessianBase(hess_method='param_shift', **kwargs)`

Bases: [`DerivativeBase`](qiskit.opflow.gradients.DerivativeBase "qiskit.opflow.gradients.derivative_base.DerivativeBase")

Deprecated: Base class for the Hessian of an expected value.

<Admonition title="Deprecated since version 0.24.0" type="danger">
  The class `qiskit.opflow.gradients.hessian_base.HessianBase` is deprecated as of qiskit-terra 0.24.0. It will be removed no earlier than 3 months after the release date. For code migration guidelines, visit [https://qisk.it/opflow\_migration](https://qisk.it/opflow_migration).
</Admonition>

**Parameters**

*   **hess\_method** (*str |* [*CircuitGradient*](qiskit.opflow.gradients.CircuitGradient "qiskit.opflow.gradients.circuit_gradients.circuit_gradient.CircuitGradient")) – The method used to compute the state/probability gradient. Can be either `'param_shift'` or `'lin_comb'` or `'fin_diff'`. Ignored for gradients w\.r.t observable parameters.
*   **kwargs** (*dict*) – Optional parameters for a CircuitGradient

**Raises**

**ValueError** – If method != `fin_diff` and `epsilon` is not None.

## Attributes

<span id="qiskit.opflow.gradients.HessianBase.hess_method" />

### hess\_method

Returns `CircuitGradient`.

**Returns**

`CircuitGradient`.
