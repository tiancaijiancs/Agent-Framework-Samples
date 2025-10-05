# Change Log - Agent Framework Samples

## 2025-10-03

### Fixed GraphViz Integration

**Summary:** Added GraphViz installation and visualization capabilities to all workflow samples

#### A. DevContainer Update

| Component | Change Description |
|-----------|-------------------|
| Development Environment | Added GraphViz system package to devcontainer configuration |
| Installation | Pre-configured GraphViz to eliminate manual setup steps |

#### B. Workflow Samples Update

***Folder*** - *07.Workflow/code_samples/python*

| File | Changes Made |
|------|--------------|
| `01.python-agent-framework-workflow-ghmodel-basic.ipynb` | • Added `sudo apt install graphviz -y` installation<br>• Integrated WorkflowViz for workflow visualization<br>• Added SVG export with `viz.export(format="svg")`<br>• Implemented inline notebook rendering with HTML fallback |
| `02.python-agent-framework-workflow-ghmodel-sequential.ipynb` | • Added GraphViz system installation commands<br>• Integrated workflow visualization for sequential pipeline<br>• Added SVG generation for three-agent workflow<br>• Implemented consistent visualization pattern |
| `03.python-agent-framework-workflow-ghmodel-concurrent.ipynb` | • Added GraphViz installation for concurrent workflows<br>• Implemented parallel execution diagram generation<br>• Added visual representation of concurrent agents<br>• Consistent SVG export functionality |
| `04.python-agent-framework-workflow-aifoundry-condition.ipynb` | • Added GraphViz support for conditional workflows<br>• Implemented decision tree diagram generation<br>• Added conditional branching visualization<br>• Consistent visualization approach |