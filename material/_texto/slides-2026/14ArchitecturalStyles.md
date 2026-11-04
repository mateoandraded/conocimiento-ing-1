# 14ArchitecturalStyles

_Fuente: `14ArchitecturalStyles.pdf`_


## Página 1

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Software Architecture and
Architectural Styles
Lecture 14
[página sin texto: revisar visualmente]

## Página 2

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Agenda
• Software Design Principles
• Architectural Design vs. Detailed Design
• Software Architecture
• Architectural Design Decisions
• Architectural Views
• Architectural Styles
• Architecture Description Language (ADL)

## Página 3

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Software Design Principles
[página sin texto: revisar visualmente]

## Página 4

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
¿Qué es diseño de software?
• Se puede referir a dos cosas: a un proceso o al resultado de este.
• “Diseño de software es un proceso que define la arquitectura,
componentes, interfaces y otras características de un sistema o
un componente”.
▪Software Engineering Body of Knowledge (SWEBOK)
• “Un diseño de software es una descripción de la estructura del
software
a
ser implementado, los
modelos
de
datos y
estructuras usadas por el sistema, las interfaces entre los
componentes del sistema y, algunas veces, los algoritmos
utilizados”.
▪Ian Sommerville

## Página 5

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Components and Connectors
• A software component is an architectural entity that
▪encapsulates a subset of the system’s functionality and/or data
▪restricts access to that subset via an explicitly defined interface
▪has explicitly defined dependencies on its required execution
context
• A software connector is an architectural building block
tasked with effecting and regulating interactions among
components

## Página 6

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Principios de diseño de software
• Los
principios
de
diseño
de
software
son
nociones
fundamentales que proveen las bases para diferentes
enfoques de diseño de software. Son siete:
▪abstracción;
▪cohesión y acoplamiento;
▪descomposición y modularización;
▪encapsulamiento/ocultamiento de información;
▪separación de interfaz e implementación;
▪suficiencia, completitud y primitivismo;
▪y separación de preocupaciones.

## Página 7

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Principios de diseño de software
1. Abstracción se refiere a la vista de un objeto enfocándose
en la información relevante a un propósito en particular e
ignorando el resto de la información.
Cortesía: Hayim Makabee, The Cat as a Metaphor in Object-Oriented Software Development

## Página 8

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Principios de diseño de software
2. Acoplamiento se define como el grado de interdependencia o
interconexión entre los módulos de un software, mientras que
cohesión se define como el grado de relación entre las
responsabilidades asignadas a un módulo.
▪Si hay alta interdependencia, entonces los cambios en un módulo
tendrán efectos significativos sobre el comportamiento de los demás.
▪Si un módulo es responsable de un número de funciones no
relacionadas, entonces las funcionalidades no han sido bien distribuidas
entre los módulos.
▪Ideal: alta cohesión y bajo acoplamiento.
Cortesía: Masudur Rahman, Recommendation of Move Method
Refactorings Using Coupling, Cohesion and Contextual Similarity

## Página 9

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Principios de diseño de software
3. Descomposición
y
modularización
significa
que
un
software es dividido en un número de componentes más
pequeños con interfaces bien definidas que describen las
interacciones entre los componentes.
▪Usualmente, el objetivo es ubicar diferentes funcionalidades y
responsabilidades en diferentes componentes.
Cortesía: Pfleeger, Software Engineering Theory and Practice

## Página 10

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Principios de diseño de software
4. Encapsulamiento y ocultamiento de información significa
agrupar y empaquetar los detalles internos de una
abstracción y hacer esos detalles inaccesibles a entidades
externas.
Cortesía: Sathasivam Karmehavannan, Encapsulation in Java programming language - Codeforcoding

## Página 11

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Principios de diseño de software
5. Separación de interfaz e implementación implica definir
un
componente
especificando
una
interfaz
pública
(conocida para los clientes) que está separada de los
detalles de cómo el componente está implementado.
Cortesía: Li An, Modeling Human Decisions in Coupled Human and Natural Systems: Review of Agent-Based Models

## Página 12

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Principios de diseño de software
6. Suficiencia,
completitud
y
primitivismo:
Alcanzar
suficiencia
y
completitud
significa
asegurar
que
un
componente de software captura todas las características
importantes para alcanzar su objetivo, no más y no menos.
Primitivismo significa que el diseño debería estar basado
en patrones que sean de fácil implementación.

## Página 13

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Principios de diseño de software
7. Separación
de
preocupaciones:
Una
preocupación
(concern) es un área de interés con respecto al diseño de
un software. La arquitectura de un software debe tener
una o varias vistas de preocupaciones que permitan a los
interesados concentrarse en pocas cosas a la vez a fin de
reducir la complejidad.
Cortesía: Willie Streeter, Practical Web Development and Architecture

## Página 14

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Architectural Design vs. Detailed Design
[página sin texto: revisar visualmente]

## Página 15

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Diseño de software
• Dos niveles de diseño de software:
1. Diseño de alto nivel o arquitectural
2. Diseño detallado
[página sin texto: revisar visualmente]

## Página 16

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Diseño de alto nivel o arquitectural
• La palabra arquitectura es a menudo utilizada en el contexto de algo a
alto nivel, es decir, está separado de detalles a bajo nivel.
• Es un enfoque de macro diseño para crear modelos que ilustren
aspectos de calidad y funciones del sistema de software.
• ¿Qué se decide en el diseño arquitectural de un software?
▪Plataforma tecnológica
▪Despliegue físico del sistema de software, incluyendo subsistemas ubicados
en diferentes lugares.
▪Selección de los principales componentes estructurales
▪La forma en la que el sistema de software, como un todo, se va a comunicar
(ej.: protocolos de comunicación)
▪Problemas de concurrencia
▪Se evalúa requerimientos no funcionales (ej.: desempeño, seguridad,
robustez, escalabilidad)
▪Entre otros

## Página 17

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Diseño detallado
• Se refina el diseño arquitectural a un punto en el que el
diseño está lo suficientemente completo como para
empezar la construcción del software.
• ¿Qué se decide en el diseño detallado de un software?
▪Se refina componentes en clases
▪Se implementan interfaces
▪Se especifica las relaciones entre clases
▪Se identifica y aplica patrones de diseño
▪Se diseña componentes y sus interfaces

## Página 18

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Software Architecture
[página sin texto: revisar visualmente]

## Página 19

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Software Architecture
• Architectural design is concerned with understanding how a
software system should be organized and designing the overall
structure of that system.
• The output of the architectural design process is an architectural
model that describes how the system is organized as a set of
communicating components.
• “A software system's architecture is the set of principal design
decisions made about the system” – Taylor et al.
• “A reference architecture is the set of principal design decisions
that are simultaneously applicable to multiple related systems,
typically within an application domain, with explicitly defined
points of variation” – Taylor et al.

## Página 20

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
A Software Architecture Example
• Each box in the diagram represents a component.
▪Boxes within boxes indicate that the component has been
decomposed to subcomponents.
▪Arrows mean that data and or control signals are passed from
component to component in the direction of the arrows.
More examples in
https://handbookofsoftwarearchitecture.com

## Página 21

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Why is Software Architecture Important?
• Software architecture is important because it affects the
performance, robustness, distributability, and maintainability
of a system.
• Individual components implement the functional system
requirements, but the dominant influence on the non-
functional system characteristics is the system’s architecture.

## Página 22

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Software Architecture
• Designing and documenting software architecture has three
advantages:
▪Stakeholder
communication
The
architecture
is
a
high-level
presentation of the system that may be used as a focus for discussion
by a range of different stakeholders.
▪System analysis Making the system architecture explicit at an early
stage in the system development requires some analysis. Architectural
design decisions have a profound effect on whether or not the system
can meet critical requirements such as performance, reliability, and
maintainability.
▪Large-scale reuse An architectural model is a compact, manageable
description of how a system is organized and how the components
interoperate. The system architecture is often the same for systems
with similar requirements and so can support large-scale software
reuse.

## Página 23

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Architectural Design Decisions
[página sin texto: revisar visualmente]

## Página 24

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Architectural Design Decisions
[página sin texto: revisar visualmente]

## Página 25

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Architectural Views
[página sin texto: revisar visualmente]

## Página 26

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Architectural Views
• It is impossible to represent all relevant information about a
system’s architecture in a single diagram, as a graphical
model can only show one view or perspective of the system.

## Página 27

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Architectural Views
1. A logical view, which shows the key abstractions in the
system as objects or object classes. It should be possible to
relate the system requirements to entities in this logical
view.
2. A process view, which shows how, at runtime, the system is
composed of interacting processes. This view is useful for
making
judgments
about
non-functional
system
characteristics such as performance and availability.

## Página 28

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Architectural Views
3. A development view, which shows how the software is
decomposed for development; that is, it shows the
breakdown of the software into components that are
implemented by a single developer or development team.
This
view
is
useful
for
software
managers
and
programmers.
4. A physical view, which shows the system hardware and
how software components are distributed across the
processors in the system. This view is useful for systems
engineers planning a system deployment.

## Página 29

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Architectural Styles
[página sin texto: revisar visualmente]

## Página 30

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Architectural Styles
• An architectural style is a named collection of architectural
design decisions that
▪are applicable in a given development context
▪constrain architectural design decisions that are specific to a
particular system within that context
▪elicit beneficial qualities in each resulting system

## Página 31

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Architectural Styles
• The architecture of a software system may be based on a
particular architectural pattern or style (these terms have
come to mean the same thing).
• However, strictly speaking…
▪Architectural styles define the components and connectors
(‘what?’)
❖Less domain specific
▪Architectural patterns define the implementation strategies of
those components and connectors (‘how?’)
❖More domain specific
• Good architecture makes use of design patterns (on a finer
granular level)

## Página 32

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Architectural Styles
• An
architectural
style
is
a
description
of
a
system
organization, such as a client–server organization or a
layered architecture.
• Architectural styles capture the essence of an architecture
that has been used in different software systems.
• You should be aware of common styles, where they can be
used, and their strengths and weaknesses when making
decisions about the architecture.
• Let us introduce a selection of architectural patterns that are
commonly used…

## Página 33

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
The Model-View-Controller (MVC) pattern
[página sin texto: revisar visualmente]

## Página 34

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
The Model-View-Controller (MVC) pattern
[página sin texto: revisar visualmente]

## Página 35

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Layered Architecture
[página sin texto: revisar visualmente]

## Página 36

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Layered Architecture
[página sin texto: revisar visualmente]

## Página 37

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Layered Architecture
[página sin texto: revisar visualmente]

## Página 38

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Repository Architecture
[página sin texto: revisar visualmente]

## Página 39

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Repository Architecture
[página sin texto: revisar visualmente]

## Página 40

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Repository Architecture
[página sin texto: revisar visualmente]

## Página 41

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Client–Server Architectural Style
[página sin texto: revisar visualmente]

## Página 42

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Client–Server Architectural Style
[página sin texto: revisar visualmente]

## Página 43

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Pipe and Filter Architecture
[página sin texto: revisar visualmente]

## Página 44

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Pipe and Filter Architecture
[página sin texto: revisar visualmente]

## Página 45

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Pipe and Filter Architecture
[página sin texto: revisar visualmente]

## Página 46

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Architecture Description Language (ADL)
[página sin texto: revisar visualmente]

## Página 47

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Architecture Description Language (ADL)
• Software architectures shift the focus of developers from
lines-of-code to coarser-grained architectural elements and
their overall interconnection structure.
• An ADL must explicitly model components, connectors, and
their configurations; furthermore, to be truly usable and
useful, it must provide tool support for architecture-based
development and evolution.

## Página 48

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Architecture Description Language (ADL)
• An ADL should exhibit the following properties:
▪ability
to
model
components,
with
property assertions,
interfaces, and implementations,
▪ability to model connectors, with protocols, property assertions,
and implementations,
▪abstraction and encapsulation,
▪types and type checking, and
▪ability to accommodate analysis tools.

## Página 49

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Architecture Description Language (ADL)
• The
focus
on conceptual architecture
and
explicit
treatment of connectors as first-class entities differentiate,
ADLs
from
MILs
(Module
Interconnection
Languages),
programming languages, and OO notations and languages
(e.g., UML)
• If certain abstractions (e.g., components and connectors)
are buried in others (e.g.,
classes),
the
architect's
job
is
made
more
(and unnecessarily)
difficult;
separating
components
from connectors,
raising
them
both
to
visibility
as
top-level abstractions, and endowing them
with certain features and limitations also raises them in
the consciousness of the designer.

## Página 50

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Architecture Description Language (ADL)
Source: “A Classification and
Comparison Framework for Software
Architecture Description Languages”
[página sin texto: revisar visualmente]

## Página 51

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Next On
[página sin texto: revisar visualmente]

## Página 52

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Take Away Points
• The seven design principles
• Architectural design vs. Detailed design
• What software architecture is and its importance
• The architectural design decisions
• The architectural views
• The subtle difference between architectural pattern and
style.
• The taxonomy of architectural styles
• What is an ADL?

## Página 53

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Further Reading
• Otero, “Software Engineering Design”
• Chapter 4: Patterns and Styles in Software Architecture
• Bass, Clements and Kazman, “Software Architecture in
Practice”
• Chapter 13: Architectural Tactics and Patterns
• Taylor, Medvidovic and Dashofy, “Software Architecture”
• Chapter 3: Basic Concepts
• Chapter 4: Designing Architectures
• Serebrenik et al., “Software Specification and Architecture”
• https://www.win.tue.nl/~aserebre/2IW80/2014-2015/

## Página 54

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Further Reading
• Ian Somerville, “Software Engineering”
• Chapter 6: Architectural Design
• Pressman and Maxim, “Software Engineering”
• Chapter 13: Architectural Design
• Medvidovic and Taylor, “A Classification and Comparison
Framework
for
Software
Architecture
Description
Languages”

## Página 55

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 5
Next Lecture
• This is the end of the module.
[página sin texto: revisar visualmente]