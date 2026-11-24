# Environment / Ambiente

Verified with CPython 3.11.5 on Windows 64-bit, using the recorded versions. `requirements.lock.txt` records the verified distribution hashes; `runtime-freeze.txt` records the environment. `requirements.txt` lists versions without platform-specific artifact hashes. Other platforms are not certified by this execution. No package installation or upgrade was performed for this audit.

Use an existing Jupyter interface and select the matching Python kernel. Start each local course notebook in its own folder; start each public student notebook in the language folder. Download the complete tree, including data.

For a new isolated environment, install the pinned dependencies with `python -m pip install --require-hashes -r requirements.lock.txt` from this directory. A compatible Jupyter front end must already be available or be installed separately. The repository does not redistribute dependency wheels.
