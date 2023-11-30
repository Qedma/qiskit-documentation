---
title: level_2_pass_manager
description: API reference for qiskit.transpiler.preset_passmanagers.level_2_pass_manager
in_page_toc_min_heading_level: 1
python_api_type: function
python_api_name: qiskit.transpiler.preset_passmanagers.level_2_pass_manager
---

# qiskit.transpiler.preset\_passmanagers.level\_2\_pass\_manager[¶](#qiskit-transpiler-preset-passmanagers-level-2-pass-manager "Permalink to this headline")

<span id="qiskit.transpiler.preset_passmanagers.level_2_pass_manager" />

`level_2_pass_manager(pass_manager_config)`

Level 2 pass manager: medium optimization by initial layout selection and gate cancellation using commutativity rules.

This pass manager applies the user-given initial layout. If none is given, a search for a perfect layout (i.e. one that satisfies all 2-qubit interactions) is conducted. If no such layout is found, qubits are laid out on the most densely connected subset which also exhibits the best gate fidelities.

The pass manager then transforms the circuit to match the coupling constraints. It is then unrolled to the basis, and any flipped cx directions are fixed. Finally, optimizations in the form of commutative gate cancellation and redundant reset removal are performed.

**Parameters**

**pass\_manager\_config** ([`PassManagerConfig`](qiskit.transpiler.PassManagerConfig "qiskit.transpiler.passmanager_config.PassManagerConfig")) – configuration of the pass manager.

**Return type**

[`StagedPassManager`](qiskit.transpiler.StagedPassManager "qiskit.transpiler.passmanager.StagedPassManager")

**Returns**

a level 2 pass manager.

**Raises**

[**TranspilerError**](qiskit.transpiler.TranspilerError "qiskit.transpiler.TranspilerError") – if the passmanager config is invalid.
