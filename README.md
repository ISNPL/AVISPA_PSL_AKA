# AVISPA_PSL_AKA
This repository includes the AVISPA simulation used for the security analysis of the paper "PLS-AKA: Physically Secure and Lightweight Authenticated Key Agreement Protocol for Wearable Devices." It provides formal verification scripts and simulation results that evaluate the protocol’s resistance against common network attacks.

### Security Analysis Using AVISPA and SPAN

We conducted the formal security analysis using **AVISPA** and **SPAN (Security Protocol Animator)**.
You can reproduce our experiments by following the steps below:

#### Steps for Reproduction

1. **Download SPAN + AVISPA VirtualBox Distribution**
   * Visit the following link: [https://people.irisa.fr/Thomas.Genet/span/](https://people.irisa.fr/Thomas.Genet/span/)
   * The page includes video and PDF tutorials to help you understand how SPAN and AVISPA work.

2. **Import the SPAN + AVISPA Disk**
   * Open **VirtualBox**, import the downloaded SPAN+AVISPA disk image, and start the virtual machine.

3. **Run the Simulation**
   * Copy the `simulation.hlpsl` file from the provided `code/` folder into SPAN.
   * Execute the simulation and check the results from the **CL-AtSe** and **OFMC** backends.
   * The HLPSL code consists of the following main components:
     * **Role** – Defines the behavior of each participant (e.g., initiator, responder, or server) and specifies message exchanges, cryptographic operations, and state transitions.
     * **Session** – Represents one instance of protocol execution, mapping roles to real entities (e.g., A → initiator, B → responder) and allowing concurrent protocol runs.
     * **Environment** – Describes the full simulation context, including all sessions, agents, and the intruder model. It also defines which identities and keys are known to the attacker.

4. **View the Results**
   * The analysis results can be found in the `result/` folder under the files:
     * `CL-AtSe.txt`
     * `OFMC.txt`
