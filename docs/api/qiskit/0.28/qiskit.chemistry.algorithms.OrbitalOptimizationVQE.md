# qiskit.chemistry.algorithms.OrbitalOptimizationVQE

<span id="undefined" />

`OrbitalOptimizationVQE(transformation, solver, initial_point=None, orbital_rotation=None, bounds=None, iterative_oo=True, iterative_oo_iterations=2)`

A ground state calculation employing the OOVQE algorithm. The Variational Quantum Eigensolver (VQE) algorithm enhanced with the Orbital Optimization (OO). The core of the approach resides in the optimization of orbitals through the AO-to-MO coefficients matrix C. In the usual VQE, the latter remains constant throughout the simulation. Here, its elements are modified according to C=Ce^(-kappa) where kappa is an anti-hermitian matrix. This transformation preserves the spectrum but modifies the amplitudes of the ground state of given operator such that in the end a given ansatz can be closest to that ground state, producing larger overlap and lower eigenvalue than conventional VQE. Kappa is parametrized and optimized inside the OOVQE in the same way as the gate angles. Therefore, at each step of OOVQE the coefficient matrix C is modified and the operator is recomputed, unlike usual VQE where operator remains constant. Iterative OO refers to optimization in two steps, first the wavefunction and then the orbitals. It allows for faster optimization as the operator is not recomputed when wavefunction is optimized. It is recommended to use the iterative method on real device/qasm simulator with noise to facilitate the convergence of the classical optimizer. For more details of this method refer to: [https://aip.scitation.org/doi/10.1063/1.5141835](https://aip.scitation.org/doi/10.1063/1.5141835)

**Parameters**

*   **transformation** (`FermionicTransformation`) – a fermionic driver to operator transformation strategy.
*   **solver** (`Union`\[`MinimumEigensolver`, `MinimumEigensolverFactory`]) – a VQE instance or a factory for the VQE solver employing any custom variational form, such as the VQEUCCSDFactory. Both need to use the UCCSD variational form.
*   **initial\_point** (`Optional`\[`ndarray`]) – An optional initial point (i.e. initial parameter values) for the optimizer. If `None` then VQE will look to the variational form for a preferred point and if not will simply compute a random one.
*   **orbital\_rotation** (`Optional`\[`OrbitalRotation`]) – instance of `OrbitalRotation` class that creates the matrices that rotate the orbitals needed to produce the rotated MO coefficients C as C = C0 \* exp(-kappa).
*   **bounds** (`Optional`\[`ndarray`]) – bounds for variational form and orbital rotation parameters given to a classical optimizer.
*   **iterative\_oo** (`bool`) – when `True` optimize first the variational form and then the orbitals, iteratively. Otherwise, the wavefunction ansatz and orbitals are optimized simultaneously.
*   **iterative\_oo\_iterations** (`int`) – number of iterations in the iterative procedure, set larger to be sure to converge to the global minimum.

**Raises**

[**AquaError**](qiskit.aqua.AquaError#qiskit.aqua.AquaError "qiskit.aqua.AquaError") – if the number of orbital optimization iterations is less or equal to zero.

<span id="undefined" />

`__init__(transformation, solver, initial_point=None, orbital_rotation=None, bounds=None, iterative_oo=True, iterative_oo_iterations=2)`

**Parameters**

*   **transformation** (`FermionicTransformation`) – a fermionic driver to operator transformation strategy.
*   **solver** (`Union`\[`MinimumEigensolver`, `MinimumEigensolverFactory`]) – a VQE instance or a factory for the VQE solver employing any custom variational form, such as the VQEUCCSDFactory. Both need to use the UCCSD variational form.
*   **initial\_point** (`Optional`\[`ndarray`]) – An optional initial point (i.e. initial parameter values) for the optimizer. If `None` then VQE will look to the variational form for a preferred point and if not will simply compute a random one.
*   **orbital\_rotation** (`Optional`\[`OrbitalRotation`]) – instance of `OrbitalRotation` class that creates the matrices that rotate the orbitals needed to produce the rotated MO coefficients C as C = C0 \* exp(-kappa).
*   **bounds** (`Optional`\[`ndarray`]) – bounds for variational form and orbital rotation parameters given to a classical optimizer.
*   **iterative\_oo** (`bool`) – when `True` optimize first the variational form and then the orbitals, iteratively. Otherwise, the wavefunction ansatz and orbitals are optimized simultaneously.
*   **iterative\_oo\_iterations** (`int`) – number of iterations in the iterative procedure, set larger to be sure to converge to the global minimum.

**Raises**

[**AquaError**](qiskit.aqua.AquaError#qiskit.aqua.AquaError "qiskit.aqua.AquaError") – if the number of orbital optimization iterations is less or equal to zero.

## Methods

|                                                                                                                                                                                          |                                                                               |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| [`__init__`](#qiskit.chemistry.algorithms.OrbitalOptimizationVQE.__init__ "qiskit.chemistry.algorithms.OrbitalOptimizationVQE.__init__")(transformation, solver\[, …])                   | **type transformation**`FermionicTransformation`                              |
| [`evaluate_operators`](#qiskit.chemistry.algorithms.OrbitalOptimizationVQE.evaluate_operators "qiskit.chemistry.algorithms.OrbitalOptimizationVQE.evaluate_operators")(state, operators) | Evaluates additional operators at the given state.                            |
| [`returns_groundstate`](#qiskit.chemistry.algorithms.OrbitalOptimizationVQE.returns_groundstate "qiskit.chemistry.algorithms.OrbitalOptimizationVQE.returns_groundstate")()              | Whether the eigensolver returns the ground state or only ground state energy. |
| [`solve`](#qiskit.chemistry.algorithms.OrbitalOptimizationVQE.solve "qiskit.chemistry.algorithms.OrbitalOptimizationVQE.solve")(driver\[, aux\_operators])                               | Compute Ground State properties.                                              |

## Attributes

|                                                                                                                                                            |                                                                               |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| [`solver`](#qiskit.chemistry.algorithms.OrbitalOptimizationVQE.solver "qiskit.chemistry.algorithms.OrbitalOptimizationVQE.solver")                         | Returns the minimum eigensolver or factory.                                   |
| [`transformation`](#qiskit.chemistry.algorithms.OrbitalOptimizationVQE.transformation "qiskit.chemistry.algorithms.OrbitalOptimizationVQE.transformation") | Returns the transformation used to obtain a qubit operator from the molecule. |

<span id="undefined" />

`evaluate_operators(state, operators)`

Evaluates additional operators at the given state.

**Parameters**

*   **state** (`Union`\[`str`, `dict`, `Result`, `list`, `ndarray`, `Statevector`, `QuantumCircuit`, `Instruction`, `OperatorBase`]) – any kind of input that can be used to specify a state. See also `StateFn` for more details.
*   **operators** (`Union`\[`WeightedPauliOperator`, `OperatorBase`, `list`, `dict`]) – either a single, list or dictionary of `WeightedPauliOperator``s or any kind of operator implementing the ``OperatorBase`.

**Return type**

`Union`\[`float`, `None`, `List`\[`Optional`\[`float`]], `Dict`\[`str`, `List`\[`Optional`\[`float`]]]]

**Returns**

The expectation value of the given operator(s). The return type will be identical to the format of the provided operators.

<span id="undefined" />

`returns_groundstate()`

Whether the eigensolver returns the ground state or only ground state energy.

**Return type**

`bool`

<span id="undefined" />

`solve(driver, aux_operators=None)`

Compute Ground State properties.

**Parameters**

*   **driver** (`BaseDriver`) – a chemistry driver object which defines the chemical problem that is to be solved by this calculation.
*   **aux\_operators** (`Union`\[`List`\[`FermionicOperator`], `List`\[`BosonicOperator`], `None`]) – Additional auxiliary operators to evaluate at the ground state. Depending on whether a fermionic or bosonic system is solved, the type of the operators must be `FermionicOperator` or `BosonicOperator`, respectively.

**Raises**

**NotImplementedError** – If an operator in `aux_operators` is not of type `FermionicOperator`.

**Return type**

`ElectronicStructureResult`

**Returns**

An eigenstate result. Depending on the transformation this can be an electronic structure or bosonic result.

<span id="undefined" />

`property solver`

Returns the minimum eigensolver or factory.

**Return type**

`Union`\[`MinimumEigensolver`, `MinimumEigensolverFactory`]

<span id="undefined" />

`property transformation`

Returns the transformation used to obtain a qubit operator from the molecule.

**Return type**

`Transformation`