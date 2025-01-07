# Dockerfile Bug: Missing requirements.txt
This repository demonstrates a common error in Dockerfiles: attempting to use a file (requirements.txt in this case) that is not present in the build context.

The original `Dockerfile` attempts to copy `requirements.txt` and install packages, but this file is missing causing the build to fail.

The `Dockerfile.fixed` shows the corrected version where a valid `requirements.txt` is included and the COPY instruction is appropriately placed after the `requirements.txt` file exists in the context.