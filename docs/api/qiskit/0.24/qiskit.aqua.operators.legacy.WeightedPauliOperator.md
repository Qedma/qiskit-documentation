<span id="qiskit-aqua-operators-legacy-weightedpaulioperator" />

# qiskit.aqua.operators.legacy.WeightedPauliOperator

<span id="undefined" />

`WeightedPauliOperator(paulis, basis=None, z2_symmetries=None, atol=1e-12, name=None)`

Weighted Pauli Operator

**Parameters**

*   **paulis** (`List`\[`List`\[`Union`\[`complex`, `Pauli`]]]) – the list of weighted Paulis, where a weighted pauli is composed of a length-2 list and the first item is the weight and the second item is the Pauli object.
*   **basis** (`Optional`\[`List`\[`Tuple`\[`object`, `List`\[`int`]]]]) – the grouping basis, each element is a tuple composed of the basis and the indices to paulis which belong to that group. e.g., if tpb basis is used, the object will be a pauli. By default, the group is equal to non-grouping, each pauli is its own basis.
*   **z2\_symmetries** (`Optional`\[`Z2Symmetries`]) – recording the z2 symmetries info
*   **atol** (`float`) – the threshold used in truncating paulis
*   **name** (`Optional`\[`str`]) – the name of operator.

<span id="undefined" />

`__init__(paulis, basis=None, z2_symmetries=None, atol=1e-12, name=None)`

**Parameters**

*   **paulis** (`List`\[`List`\[`Union`\[`complex`, `Pauli`]]]) – the list of weighted Paulis, where a weighted pauli is composed of a length-2 list and the first item is the weight and the second item is the Pauli object.
*   **basis** (`Optional`\[`List`\[`Tuple`\[`object`, `List`\[`int`]]]]) – the grouping basis, each element is a tuple composed of the basis and the indices to paulis which belong to that group. e.g., if tpb basis is used, the object will be a pauli. By default, the group is equal to non-grouping, each pauli is its own basis.
*   **z2\_symmetries** (`Optional`\[`Z2Symmetries`]) – recording the z2 symmetries info
*   **atol** (`float`) – the threshold used in truncating paulis
*   **name** (`Optional`\[`str`]) – the name of operator.

## Methods

|                                                                                                                                                                                                                         |                                                                                                                                                                                                                                                                                                                                                                           |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [`__init__`](#qiskit.aqua.operators.legacy.WeightedPauliOperator.__init__ "qiskit.aqua.operators.legacy.WeightedPauliOperator.__init__")(paulis\[, basis, z2\_symmetries, …])                                           | **type paulis**`List`\[`List`\[`Union`\[`complex`, `Pauli`]]]                                                                                                                                                                                                                                                                                                             |
| [`add`](#qiskit.aqua.operators.legacy.WeightedPauliOperator.add "qiskit.aqua.operators.legacy.WeightedPauliOperator.add")(other\[, copy])                                                                               | Perform self + other.                                                                                                                                                                                                                                                                                                                                                     |
| [`anticommute_with`](#qiskit.aqua.operators.legacy.WeightedPauliOperator.anticommute_with "qiskit.aqua.operators.legacy.WeightedPauliOperator.anticommute_with")(other)                                                 | Anti commutes with                                                                                                                                                                                                                                                                                                                                                        |
| [`chop`](#qiskit.aqua.operators.legacy.WeightedPauliOperator.chop "qiskit.aqua.operators.legacy.WeightedPauliOperator.chop")(\[threshold, copy])                                                                        | Eliminate the real and imagine part of weight in each pauli by threshold.                                                                                                                                                                                                                                                                                                 |
| [`commute_with`](#qiskit.aqua.operators.legacy.WeightedPauliOperator.commute_with "qiskit.aqua.operators.legacy.WeightedPauliOperator.commute_with")(other)                                                             | Commutes with                                                                                                                                                                                                                                                                                                                                                             |
| [`construct_evaluation_circuit`](#qiskit.aqua.operators.legacy.WeightedPauliOperator.construct_evaluation_circuit "qiskit.aqua.operators.legacy.WeightedPauliOperator.construct_evaluation_circuit")(wave\_function, …) | Construct the circuits for evaluation, which calculating the expectation \<psi\|H\|psi>.                                                                                                                                                                                                                                                                                  |
| [`copy`](#qiskit.aqua.operators.legacy.WeightedPauliOperator.copy "qiskit.aqua.operators.legacy.WeightedPauliOperator.copy")()                                                                                          | Get a copy of self                                                                                                                                                                                                                                                                                                                                                        |
| [`evaluate_with_result`](#qiskit.aqua.operators.legacy.WeightedPauliOperator.evaluate_with_result "qiskit.aqua.operators.legacy.WeightedPauliOperator.evaluate_with_result")(result, statevector\_mode)                 | This method can be only used with the circuits generated by the [`construct_evaluation_circuit()`](#qiskit.aqua.operators.legacy.WeightedPauliOperator.construct_evaluation_circuit "qiskit.aqua.operators.legacy.WeightedPauliOperator.construct_evaluation_circuit") method with the same circuit\_name\_prefix name since the circuit names are tied to some meanings. |
| [`evaluate_with_statevector`](#qiskit.aqua.operators.legacy.WeightedPauliOperator.evaluate_with_statevector "qiskit.aqua.operators.legacy.WeightedPauliOperator.evaluate_with_statevector")(quantum\_state)             | **param quantum\_state**a quantum state.                                                                                                                                                                                                                                                                                                                                  |
| [`evaluation_instruction`](#qiskit.aqua.operators.legacy.WeightedPauliOperator.evaluation_instruction "qiskit.aqua.operators.legacy.WeightedPauliOperator.evaluation_instruction")(statevector\_mode\[, …])             | **param statevector\_mode**will it be run on statevector simulator or not                                                                                                                                                                                                                                                                                                 |
| [`evolve`](#qiskit.aqua.operators.legacy.WeightedPauliOperator.evolve "qiskit.aqua.operators.legacy.WeightedPauliOperator.evolve")(\[state\_in, evo\_time, …])                                                          | Carry out the eoh evolution for the operator under supplied specifications.                                                                                                                                                                                                                                                                                               |
| [`evolve_instruction`](#qiskit.aqua.operators.legacy.WeightedPauliOperator.evolve_instruction "qiskit.aqua.operators.legacy.WeightedPauliOperator.evolve_instruction")(\[evo\_time, …])                                 | Carry out the eoh evolution for the operator under supplied specifications.                                                                                                                                                                                                                                                                                               |
| [`from_dict`](#qiskit.aqua.operators.legacy.WeightedPauliOperator.from_dict "qiskit.aqua.operators.legacy.WeightedPauliOperator.from_dict")(dictionary\[, before\_04])                                                  | Load paulis from a dictionary to construct an Operator.                                                                                                                                                                                                                                                                                                                   |
| [`from_file`](#qiskit.aqua.operators.legacy.WeightedPauliOperator.from_file "qiskit.aqua.operators.legacy.WeightedPauliOperator.from_file")(file\_name\[, before\_04])                                                  | Load paulis in a file to construct an Operator.                                                                                                                                                                                                                                                                                                                           |
| [`from_list`](#qiskit.aqua.operators.legacy.WeightedPauliOperator.from_list "qiskit.aqua.operators.legacy.WeightedPauliOperator.from_list")(paulis\[, weights, name])                                                   | Create a WeightedPauliOperator via a pair of list.                                                                                                                                                                                                                                                                                                                        |
| [`is_empty`](#qiskit.aqua.operators.legacy.WeightedPauliOperator.is_empty "qiskit.aqua.operators.legacy.WeightedPauliOperator.is_empty")()                                                                              | Check Operator is empty or not.                                                                                                                                                                                                                                                                                                                                           |
| [`multiply`](#qiskit.aqua.operators.legacy.WeightedPauliOperator.multiply "qiskit.aqua.operators.legacy.WeightedPauliOperator.multiply")(other)                                                                         | Perform self \* other, and the phases are tracked.                                                                                                                                                                                                                                                                                                                        |
| [`print_details`](#qiskit.aqua.operators.legacy.WeightedPauliOperator.print_details "qiskit.aqua.operators.legacy.WeightedPauliOperator.print_details")()                                                               | Print out the operator in details.                                                                                                                                                                                                                                                                                                                                        |
| [`reorder_paulis`](#qiskit.aqua.operators.legacy.WeightedPauliOperator.reorder_paulis "qiskit.aqua.operators.legacy.WeightedPauliOperator.reorder_paulis")()                                                            | Reorder the paulis based on the basis and return the reordered paulis.                                                                                                                                                                                                                                                                                                    |
| [`rounding`](#qiskit.aqua.operators.legacy.WeightedPauliOperator.rounding "qiskit.aqua.operators.legacy.WeightedPauliOperator.rounding")(decimals\[, copy])                                                             | Rounding the weight.                                                                                                                                                                                                                                                                                                                                                      |
| [`simplify`](#qiskit.aqua.operators.legacy.WeightedPauliOperator.simplify "qiskit.aqua.operators.legacy.WeightedPauliOperator.simplify")(\[copy])                                                                       | Merge the paulis whose bases are identical and the pauli with zero coefficient would be removed.                                                                                                                                                                                                                                                                          |
| [`sub`](#qiskit.aqua.operators.legacy.WeightedPauliOperator.sub "qiskit.aqua.operators.legacy.WeightedPauliOperator.sub")(other\[, copy])                                                                               | Perform self - other.                                                                                                                                                                                                                                                                                                                                                     |
| [`to_dict`](#qiskit.aqua.operators.legacy.WeightedPauliOperator.to_dict "qiskit.aqua.operators.legacy.WeightedPauliOperator.to_dict")()                                                                                 | Save operator to a dict in pauli representation.                                                                                                                                                                                                                                                                                                                          |
| [`to_file`](#qiskit.aqua.operators.legacy.WeightedPauliOperator.to_file "qiskit.aqua.operators.legacy.WeightedPauliOperator.to_file")(file\_name)                                                                       | Save operator to a file in pauli representation.                                                                                                                                                                                                                                                                                                                          |
| [`to_opflow`](#qiskit.aqua.operators.legacy.WeightedPauliOperator.to_opflow "qiskit.aqua.operators.legacy.WeightedPauliOperator.to_opflow")(\[reverse\_endianness])                                                     | to op flow                                                                                                                                                                                                                                                                                                                                                                |

## Attributes

|                                                                                                                                                         |                                             |
| ------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------- |
| [`atol`](#qiskit.aqua.operators.legacy.WeightedPauliOperator.atol "qiskit.aqua.operators.legacy.WeightedPauliOperator.atol")                            | get atol                                    |
| [`basis`](#qiskit.aqua.operators.legacy.WeightedPauliOperator.basis "qiskit.aqua.operators.legacy.WeightedPauliOperator.basis")                         | returns basis                               |
| [`name`](#qiskit.aqua.operators.legacy.WeightedPauliOperator.name "qiskit.aqua.operators.legacy.WeightedPauliOperator.name")                            | returns name                                |
| [`num_qubits`](#qiskit.aqua.operators.legacy.WeightedPauliOperator.num_qubits "qiskit.aqua.operators.legacy.WeightedPauliOperator.num_qubits")          | Number of qubits required for the operator. |
| [`paulis`](#qiskit.aqua.operators.legacy.WeightedPauliOperator.paulis "qiskit.aqua.operators.legacy.WeightedPauliOperator.paulis")                      | get paulis                                  |
| [`z2_symmetries`](#qiskit.aqua.operators.legacy.WeightedPauliOperator.z2_symmetries "qiskit.aqua.operators.legacy.WeightedPauliOperator.z2_symmetries") | returns z2 symmetries                       |

<span id="undefined" />

`add(other, copy=False)`

Perform self + other.

**Parameters**

*   **other** ([*WeightedPauliOperator*](#qiskit.aqua.operators.legacy.WeightedPauliOperator "qiskit.aqua.operators.legacy.WeightedPauliOperator")) – to-be-combined operator
*   **copy** (*bool*) – working on a copy or self, if False, the results are written back to self.

**Returns**

operator

**Return type**

[WeightedPauliOperator](#qiskit.aqua.operators.legacy.WeightedPauliOperator "qiskit.aqua.operators.legacy.WeightedPauliOperator")

<span id="undefined" />

`anticommute_with(other)`

Anti commutes with

<span id="undefined" />

`property atol`

get atol

<span id="undefined" />

`property basis`

returns basis

<span id="undefined" />

`chop(threshold=None, copy=False)`

Eliminate the real and imagine part of weight in each pauli by threshold. If pauli’s weight is less then threshold in both real and imaginary parts, the pauli is removed.

<Admonition title="Note" type="note">
  If weight is real-only, the imaginary part is skipped.
</Admonition>

**Parameters**

*   **threshold** (*float*) – the threshold is used to remove the paulis
*   **copy** (*bool*) – chop on a copy or self

**Returns**

**if copy is True, the original operator is unchanged; otherwise,**

the operator is mutated.

**Return type**

[WeightedPauliOperator](#qiskit.aqua.operators.legacy.WeightedPauliOperator "qiskit.aqua.operators.legacy.WeightedPauliOperator")

<span id="undefined" />

`commute_with(other)`

Commutes with

<span id="undefined" />

`construct_evaluation_circuit(wave_function, statevector_mode, qr=None, cr=None, use_simulator_snapshot_mode=False, circuit_name_prefix='')`

Construct the circuits for evaluation, which calculating the expectation \<psi|H|psi>.

At statevector mode: to simplify the computation, we do not build the whole circuit for \<psi|H|psi>, instead of that we construct an individual circuit \<psi|, and a bundle circuit for H|psi>

**Parameters**

*   **wave\_function** ([*QuantumCircuit*](qiskit.circuit.QuantumCircuit#qiskit.circuit.QuantumCircuit "qiskit.circuit.QuantumCircuit")) – the quantum circuit.
*   **statevector\_mode** (*bool*) – indicate which type of simulator are going to use.
*   **qr** ([*QuantumRegister*](qiskit.circuit.QuantumRegister#qiskit.circuit.QuantumRegister "qiskit.circuit.QuantumRegister")*, optional*) – the quantum register associated with the input\_circuit
*   **cr** ([*ClassicalRegister*](qiskit.circuit.ClassicalRegister#qiskit.circuit.ClassicalRegister "qiskit.circuit.ClassicalRegister")*, optional*) – the classical register associated with the input\_circuit
*   **use\_simulator\_snapshot\_mode** (*bool, optional*) – if aer\_provider is used, we can do faster evaluation for pauli mode on statevector simulation
*   **circuit\_name\_prefix** (*str, optional*) – a prefix of circuit name

**Returns**

**a list of quantum circuits and each circuit with a unique name:**

circuit\_name\_prefix + Pauli string

**Return type**

list\[[QuantumCircuit](qiskit.circuit.QuantumCircuit#qiskit.circuit.QuantumCircuit "qiskit.circuit.QuantumCircuit")]

**Raises**

*   [**AquaError**](qiskit.aqua.AquaError#qiskit.aqua.AquaError "qiskit.aqua.AquaError") – if Operator is empty
*   [**AquaError**](qiskit.aqua.AquaError#qiskit.aqua.AquaError "qiskit.aqua.AquaError") – if quantum register is not provided explicitly and cannot find quantum register with q as the name
*   [**AquaError**](qiskit.aqua.AquaError#qiskit.aqua.AquaError "qiskit.aqua.AquaError") – The provided qr is not in the wave\_function

<span id="undefined" />

`copy()`

Get a copy of self

<span id="undefined" />

`evaluate_with_result(result, statevector_mode, use_simulator_snapshot_mode=False, circuit_name_prefix='')`

This method can be only used with the circuits generated by the [`construct_evaluation_circuit()`](#qiskit.aqua.operators.legacy.WeightedPauliOperator.construct_evaluation_circuit "qiskit.aqua.operators.legacy.WeightedPauliOperator.construct_evaluation_circuit") method with the same circuit\_name\_prefix name since the circuit names are tied to some meanings.

Calculate the evaluated value with the measurement results.

**Parameters**

*   **result** (*qiskit.Result*) – the result from the backend.
*   **statevector\_mode** (*bool*) – indicate which type of simulator are used.
*   **use\_simulator\_snapshot\_mode** (*bool*) – if aer\_provider is used, we can do faster evaluation for pauli mode on statevector simulation
*   **circuit\_name\_prefix** (*str*) – a prefix of circuit name

**Returns**

the mean value float: the standard deviation

**Return type**

float

**Raises**

[**AquaError**](qiskit.aqua.AquaError#qiskit.aqua.AquaError "qiskit.aqua.AquaError") – if Operator is empty

<span id="undefined" />

`evaluate_with_statevector(quantum_state)`

**Parameters**

**quantum\_state** (*numpy.ndarray*) – a quantum state.

**Returns**

the mean value float: the standard deviation

**Return type**

float

**Raises**

[**AquaError**](qiskit.aqua.AquaError#qiskit.aqua.AquaError "qiskit.aqua.AquaError") – if Operator is empty

<span id="undefined" />

`evaluation_instruction(statevector_mode, use_simulator_snapshot_mode=False)`

**Parameters**

*   **statevector\_mode** (*bool*) – will it be run on statevector simulator or not
*   **use\_simulator\_snapshot\_mode** (*bool*) – will it use qiskit aer simulator operator mode

**Returns**

Pauli-instruction pair.

**Return type**

dict

**Raises**

*   [**AquaError**](qiskit.aqua.AquaError#qiskit.aqua.AquaError "qiskit.aqua.AquaError") – if Operator is empty
*   [**MissingOptionalLibraryError**](qiskit.aqua.MissingOptionalLibraryError#qiskit.aqua.MissingOptionalLibraryError "qiskit.aqua.MissingOptionalLibraryError") – qiskit-aer not installed

<span id="undefined" />

`evolve(state_in=None, evo_time=0, num_time_slices=1, quantum_registers=None, expansion_mode='trotter', expansion_order=1)`

Carry out the eoh evolution for the operator under supplied specifications.

**Parameters**

*   **state\_in** ([*QuantumCircuit*](qiskit.circuit.QuantumCircuit#qiskit.circuit.QuantumCircuit "qiskit.circuit.QuantumCircuit")) – a circuit describes the input state
*   **evo\_time** (*Union(complex, float,* [*Parameter*](qiskit.circuit.Parameter#qiskit.circuit.Parameter "qiskit.circuit.Parameter")*,* [*ParameterExpression*](qiskit.circuit.ParameterExpression#qiskit.circuit.ParameterExpression "qiskit.circuit.ParameterExpression")*)*) – The evolution time
*   **num\_time\_slices** (*int*) – The number of time slices for the expansion
*   **quantum\_registers** ([*QuantumRegister*](qiskit.circuit.QuantumRegister#qiskit.circuit.QuantumRegister "qiskit.circuit.QuantumRegister")) – The QuantumRegister to build the QuantumCircuit off of
*   **expansion\_mode** (*str*) – The mode under which the expansion is to be done. Currently support ‘trotter’, which follows the expansion as discussed in [http://science.sciencemag.org/content/273/5278/1073](http://science.sciencemag.org/content/273/5278/1073), and ‘suzuki’, which corresponds to the discussion in [https://arxiv.org/pdf/quant-ph/0508139.pdf](https://arxiv.org/pdf/quant-ph/0508139.pdf)
*   **expansion\_order** (*int*) – The order for suzuki expansion

**Returns**

The constructed circuit.

**Return type**

[QuantumCircuit](qiskit.circuit.QuantumCircuit#qiskit.circuit.QuantumCircuit "qiskit.circuit.QuantumCircuit")

**Raises**

*   [**AquaError**](qiskit.aqua.AquaError#qiskit.aqua.AquaError "qiskit.aqua.AquaError") – quantum\_registers must be in the provided state\_in circuit
*   [**AquaError**](qiskit.aqua.AquaError#qiskit.aqua.AquaError "qiskit.aqua.AquaError") – if operator is empty

<span id="undefined" />

`evolve_instruction(evo_time=0, num_time_slices=1, expansion_mode='trotter', expansion_order=1)`

Carry out the eoh evolution for the operator under supplied specifications.

**Parameters**

*   **evo\_time** (*Union(complex, float,* [*Parameter*](qiskit.circuit.Parameter#qiskit.circuit.Parameter "qiskit.circuit.Parameter")*,* [*ParameterExpression*](qiskit.circuit.ParameterExpression#qiskit.circuit.ParameterExpression "qiskit.circuit.ParameterExpression")*)*) – The evolution time
*   **num\_time\_slices** (*int*) – The number of time slices for the expansion
*   **expansion\_mode** (*str*) – The mode under which the expansion is to be done. Currently support ‘trotter’, which follows the expansion as discussed in [http://science.sciencemag.org/content/273/5278/1073](http://science.sciencemag.org/content/273/5278/1073), and ‘suzuki’, which corresponds to the discussion in [https://arxiv.org/pdf/quant-ph/0508139.pdf](https://arxiv.org/pdf/quant-ph/0508139.pdf)
*   **expansion\_order** (*int*) – The order for suzuki expansion

**Returns**

The constructed QuantumCircuit.

**Return type**

[QuantumCircuit](qiskit.circuit.QuantumCircuit#qiskit.circuit.QuantumCircuit "qiskit.circuit.QuantumCircuit")

**Raises**

*   **ValueError** – Number of time slices should be a non-negative integer
*   **NotImplementedError** – expansion mode not supported
*   [**AquaError**](qiskit.aqua.AquaError#qiskit.aqua.AquaError "qiskit.aqua.AquaError") – if operator is empty

<span id="undefined" />

`classmethod from_dict(dictionary, before_04=False)`

Load paulis from a dictionary to construct an Operator. The dictionary must comprise the key ‘paulis’ having a value which is an array of pauli dicts. Each dict in this array must be represented by label and coeff (real and imag) such as in the following example:

```python
{'paulis':
    [
        {'label': 'IIII',
         'coeff': {'real': -0.33562957575267038, 'imag': 0.0}},
        {'label': 'ZIII',
         'coeff': {'real': 0.28220597164664896, 'imag': 0.0}},
         ...
    ]
 }
```

**Parameters**

*   **dictionary** (*dict*) – dictionary, which contains a list of Paulis and coefficients.
*   **before\_04** (*bool*) – support the format before Aqua 0.4.

**Returns**

the operator created from the input dictionary.

**Return type**

[WeightedPauliOperator](#qiskit.aqua.operators.legacy.WeightedPauliOperator "qiskit.aqua.operators.legacy.WeightedPauliOperator")

**Raises**

[**AquaError**](qiskit.aqua.AquaError#qiskit.aqua.AquaError "qiskit.aqua.AquaError") – Invalid dictionary

<span id="undefined" />

`classmethod from_file(file_name, before_04=False)`

Load paulis in a file to construct an Operator.

**Parameters**

*   **file\_name** (*str*) – path to the file, which contains a list of Paulis and coefficients.
*   **before\_04** (*bool*) – support the format before Aqua 0.4.

**Returns**

the loaded operator.

**Return type**

[WeightedPauliOperator](#qiskit.aqua.operators.legacy.WeightedPauliOperator "qiskit.aqua.operators.legacy.WeightedPauliOperator")

<span id="undefined" />

`classmethod from_list(paulis, weights=None, name=None)`

Create a WeightedPauliOperator via a pair of list.

**Parameters**

*   **paulis** (*list\[*[*Pauli*](qiskit.quantum_info.Pauli#qiskit.quantum_info.Pauli "qiskit.quantum_info.Pauli")*]*) – the list of Paulis
*   **weights** (*list\[complex], optional*) – the list of weights, if it is None, all weights are 1.
*   **name** (*str, optional*) – name of the operator.

**Returns**

operator

**Return type**

[WeightedPauliOperator](#qiskit.aqua.operators.legacy.WeightedPauliOperator "qiskit.aqua.operators.legacy.WeightedPauliOperator")

**Raises**

**ValueError** – The length of weights and paulis must be the same

<span id="undefined" />

`is_empty()`

Check Operator is empty or not.

**Returns**

True if empty, False otherwise

**Return type**

bool

<span id="undefined" />

`multiply(other)`

Perform self \* other, and the phases are tracked.

**Parameters**

**other** ([*WeightedPauliOperator*](#qiskit.aqua.operators.legacy.WeightedPauliOperator "qiskit.aqua.operators.legacy.WeightedPauliOperator")) – an operator

**Returns**

the multiplied operator

**Return type**

[WeightedPauliOperator](#qiskit.aqua.operators.legacy.WeightedPauliOperator "qiskit.aqua.operators.legacy.WeightedPauliOperator")

<span id="undefined" />

`property name`

returns name

<span id="undefined" />

`property num_qubits`

Number of qubits required for the operator.

**Returns**

number of qubits

**Return type**

int

<span id="undefined" />

`property paulis`

get paulis

<span id="undefined" />

`print_details()`

Print out the operator in details.

**Returns**

a formatted string describes the operator.

**Return type**

str

<span id="undefined" />

`reorder_paulis()`

Reorder the paulis based on the basis and return the reordered paulis.

**Return type**

`List`\[`List`\[`Union`\[`complex`, `Pauli`]]]

**Returns**

the ordered paulis based on the basis.

<span id="undefined" />

`rounding(decimals, copy=False)`

Rounding the weight.

**Parameters**

*   **decimals** (*int*) – rounding the weight to the decimals.
*   **copy** (*bool*) – chop on a copy or self

**Returns**

operator

**Return type**

[WeightedPauliOperator](#qiskit.aqua.operators.legacy.WeightedPauliOperator "qiskit.aqua.operators.legacy.WeightedPauliOperator")

<span id="undefined" />

`simplify(copy=False)`

Merge the paulis whose bases are identical and the pauli with zero coefficient would be removed.

<Admonition title="Note" type="note">
  This behavior of this method is slightly changed, it will remove the paulis whose weights are zero.
</Admonition>

**Parameters**

**copy** (*bool*) – simplify on a copy or self

**Returns**

the simplified operator

**Return type**

[WeightedPauliOperator](#qiskit.aqua.operators.legacy.WeightedPauliOperator "qiskit.aqua.operators.legacy.WeightedPauliOperator")

<span id="undefined" />

`sub(other, copy=False)`

Perform self - other.

**Parameters**

*   **other** ([*WeightedPauliOperator*](#qiskit.aqua.operators.legacy.WeightedPauliOperator "qiskit.aqua.operators.legacy.WeightedPauliOperator")) – to-be-combined operator
*   **copy** (*bool*) – working on a copy or self, if False, the results are written back to self.

**Returns**

operator

**Return type**

[WeightedPauliOperator](#qiskit.aqua.operators.legacy.WeightedPauliOperator "qiskit.aqua.operators.legacy.WeightedPauliOperator")

<span id="undefined" />

`to_dict()`

Save operator to a dict in pauli representation.

**Returns**

a dictionary contains an operator with pauli representation.

**Return type**

dict

<span id="undefined" />

`to_file(file_name)`

Save operator to a file in pauli representation.

**Parameters**

**file\_name** (*str*) – path to the file

<span id="undefined" />

`to_opflow(reverse_endianness=False)`

to op flow

<span id="undefined" />

`property z2_symmetries`

returns z2 symmetries