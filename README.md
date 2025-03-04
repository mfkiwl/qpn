[![QP-nano framework](https://www.state-machine.com/img/qpn_banner.jpg)](https://www.state-machine.com)

> **NOTE:** If your company has a policy forbidding open source in your
product, all QP frameworks can be
[licensed commercially](https://www.state-machine.com/licensing),
in which case you don't use any open source license and you do not violate
your policy.


---------------------------------------------------------------------------
# What's New?

**NOTE** QP-nano has been **discontinued** from active development
and support and is **not recommended** for new designs. This QP-nano
repository is preserved for the existing user base.


---------------------------------------------------------------------------
# Documentation
The offline HTML documentation for **this** particular version of QP-nano
is located in the folder html/. To view the offline documentation, open
the file html/index.html in your web browser.

The online HTML documention for the **latest** version of QP-nano is located
at: https://www.state-machine.com/qpn/


---------------------------------------------------------------------------
# About QP-nano
QP-nano (Quantum Platform Nano) is an ultra-lightweight, open source
[Real-Time Embedded Framework (RTEF)][RTEF] for building modern embedded
software as systems of asynchronous, event-driven [active objects][Active]
(actors). The [QP-nano] framework is a member of a larger [QP] family
consisting of [QP/C], [QP/C++], and [QP-nano] frameworks, which are all
strictly quality controlled, thoroughly documented, and [commercially
licensable][Lic].

## Safer Model of Concurrency
The [QP] framework family is based on the [Active Object][Active] (**actor**)
design pattern, which inherently supports and automatically enforces the
following best practices of concurrent programming:

- Keep data isolated and bound to active objects' threads. Threads should
hide (**encapsulate**) their private data and other resources, and not
share them with the rest of the system.

- Communicate among active object threads **asynchronously** via event
objects. Using asynchronous events keeps the threads running truly
independently, **without blocking** on each other.

- Active object threads should spend their lifetime responding to incoming
events, so their mainline should consist of an **event-loop** that handles
events one at a time (to completion), thus avoiding any concurrency hazards
within an active object thread itself.

This architecture is generally **safer**, more responsive and easier to
understand and maintain than the shared-state concurrency of a conventional
RTOS. It also provides higher level of abstraction and the *correct*
abstractions to effectively apply **modeling** and **code generation** to
deeply embedded real-time systems.

## Hierarchical State Machines
The behavior of active objects is specified in QP-nano by means of
[Hierarchical State Machines][HSM] (UML statecharts). The framework
supports manual coding of UML state machines in C as well as automatic
**code generation** by means of the free [QM modeling tool][QM].

## Built-in Real-Time Kernels
The QP-nano framework can run on bare-metal single-chip microcontrollers,
completely replacing a traditional "superloop" or an RTOS. The framework
contains a selection of **built-in real-time kernels**, such as the
cooperative QV-nano kernel and the preemptive non-blocking QK-nano kernel.
Native QP-nano ports and ready-to-use examples are provided for such CPUs
MSP430, AVRmega, and ARM Cortex-M (M0/M0+/M3/M4).

## Maturity
With 60,000 downloads a year, the [QP] family is the most popular such
solution on the embedded software market. It provides a modern, reusable
architecture for embedded applications, which combines the active-object
model of concurrency with hierarchical state machines.

---------------------------------------------------------------------------
# Getting Started with QP-nano
The [QP-nano Reference Manual](https://www.state-machine.com/qpn/) provides
instructions on how to download, install, and get started with QP-nano quickly.

The [AppNote: "Getting Started with QP-nano"][AN] contains also a tutorial,
in which you build a simple "Blinky" application.


---------------------------------------------------------------------------
# QP-nano Licensing
QP-nano is licensed under the increasingly popular [dual licensing model][Lic],
in which both the open source software distribution mechanism and
traditional closed source software distribution models are combined.

> **NOTE:** If your company has a policy forbidding open source in your
product, all QP frameworks can be [licensed commercially][Lic], in which case
you don't use any open source license and you do not violate your policy.

---------------------------------------------------------------------------
# QP-nano Documentation
The **QP-nano Manual** is located online at: https://www.state-machine.com/qpn

---------------------------------------------------------------------------
# 3rd-Party QP-nano Ports/Adaptations

[<b>QPN-PIC16</b>](https://github.com/aschatte/qpn) is an adaptation of the QP-nano framework to the [Microchip PIC16](https://www.microchip.com/en-us/products/microcontrollers-and-microprocessors/8-bit-mcus/pic-mcus) architecture as compiled by the MPALB-X IDE using the XC8 compiler (C90/C99). It allows QP-nano models developed using the QM modeling tool to be integrated with the QV-nano kernel to build [Active Object](https://www.state-machine.com/active-object) applications. The very limited resources of the PIC16 family of MCUs, primarily the hardware stack, required a special version of QP-nano and a QM-Modeler editing post-processor, `QM2HSM.exe`, to effect.



---------------------------------------------------------------------------
# How to get help?
- [Free Support Forum](https://sourceforge.net/p/qpc/discussion/668726)
- [Bug Reports](https://sourceforge.net/p/qpc/bugs/)
- [Feature Requests](https://sourceforge.net/p/qpc/feature-requests/)
- [Quantum Leaps website](https://www.state-machine.com)
- [Quantum Leaps licensing](https://www.state-machine.com/licensing)
- [info@state-machine.com](mailto:info@state-machine.com)

   [RTEF]: <https://www.state-machine.com/doc/concepts#RTEF>
   [QP]: <https://www.state-machine.com/products/#QP>
   [QP/C]: <https://www.state-machine.com/qpc>
   [QP/C++]: <https://www.state-machine.com/qpcpp>
   [QP-nano]: <https://www.state-machine.com/qpn>
   [QM]: <https://www.state-machine.com/qm>
   [Active]: <https://www.state-machine.com/doc/concepts#Active>
   [HSM]: <https://www.state-machine.com/doc/concepts#HSM>
   [Lic]: <https://www.state-machine.com/licensing>
   [AN]: <https://www.state-machine.com/doc/AN_Getting_Started_with_QP-nano.pdf>
