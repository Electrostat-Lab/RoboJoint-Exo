## Part.02: Software Architectural Subsystems Detailed Design
  * 2.1 Review Software Architecture: Subsystems, Components, Modules, and Teams.
  * 2.3 Deliverable Milestones and a general roadmap.
  * 2.4 Hardware-Software Abstraction Layer (HSAL): Subsystems and their components.
  * 2.5 Hardware-Software Abstraction Layer (HSAL): Mathematical Model design and implementation.
  * 2.7 Hardware-Software Abstraction Layer (HSAL): Physical Model design and implementation.
  * 2.8 Hardware-Software Abstraction Layer (HSAL): Wiring Circuitry and hardware protocols.
  * 2.9 Hardware-Software Abstraction Layer (HSAL): Software AI Module design and implementation.
  * 3.1 RoboExo-Simulator Subsystem: Core components design and implementation.
  * 3.2 RoboExo-Hardware Subsystem: Core components design and implementation.

### 2.1 Review Software Architecture: Subsystems, Components, Modules, and Teams
**Preface:**
In the previous document, an overview of the system design has been explained; in this document, a further breakdown to the hardware/software design subsystems and components will be attained. Two engineering modelling strategies are being utilized here; the **System-Entity-Structure/Model-Base (SES/MB)** to explain the abstract skeleton of the system, its subsystems, and their components and the relations among them, and the **Automata Theory**, particularly a free model of the primitive **Finite-Automata** to better explain the relation among components from the same subsystem or from different subsystems. For an in-depth exploration of the various subsystems of the Robo-Exo Device; refer to **Section 2.4**.

> [!IMPORTANT]
>
> Transition keywords from the problem analysis to the full system design:
> 1) A system module represents a **Subsystem**.
> 2) A system module or a subsystem is a collection of system components.
> 3) Relations among system components are modelled using the automata theory.
> 4) Relations among system components represent algorithms. 

<img src="https://github.com/RoboJoint-Team/RoboJoint-Exo/blob/main/system-design/assets/solution-design.svg">

### 2.4 Hardware-Software Abstraction Layer (HSAL): Subsystems and their components
**HSAL Subsystems:**
* Vector Math Subsystem (Arithmos): This subsystem is comprised of `(1) 2D Vector Transforms. (2) 3D Vector Transforms. (3) Soft IRQs Component.`
* Matrix Algebra Subsytem (Arithmos): This subsystem is comprised of `(1) N-Dimensional Matrix Transforms. (2) 3D Matrix Rotator Transformer. (3) Matrix Gimbal Component. (4) Soft IRQs Component`.
* 3D Physics Subsystem (Delta-Engine): This subsystem is comprised of `(1) Physics Spaces. (2) Newtonian Classical Mechanics. (3) Biomechanics Specialization. (4) Joint Builder Component.`.

**Simulator Subsystems:**
* 3D Physics Glue Subsystem: This subsystem is comprised of `(1) JNI/C Interpreter Component. (2) JVM Delta Components.`.
* Game Engine Subsystems: This subsystem is comprised of `(1) Delta-to-Minie Interpreter Component. (2) Game States Components.`.

**Hardware Subsystems:**
* Processor Subsystem.
* 3D Physics Glue Subsystem.
* Sensors Subsystem.
* Joint Module Subsystem.
* Battery Subsystem.
* Comm Subsystem.
* Fault-tolerance subsystem.
