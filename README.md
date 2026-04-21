# Monopoly Deal Card Game - Phase 1 UML Diagrams

Welcome to the UML repository for our Monopoly Deal Card Game project (Phase 1). 

Since PDF compilers (like Overleaf) often compress large vector graphics or restrict canvas sizes, we have created this repository to provide you with **High-Resolution, uncompressed SVG versions** of our system models. 

You can click on any `.svg` file above to view it in full detail. You can freely zoom in to inspect the method calls, parameters, and structural relationships.

## Repository Contents

This repository contains all 8 UML diagrams referenced in our Phase-1 Document, organized into three categories:

### 1. Use Case Diagrams (FR Validation)
* **`Fig1_UseCase_GlobalGameFlow.svg`**: Illustrates the complete game lifecycle with a clear distinction between **Human Players** and **AI Players**. It covers integrated turn-management logic, including setup, turn-cycle execution, and win-condition automated checks.
* **`Fig2_UseCase_ActionCardDetails.svg`**: A detailed sub-system view using `<<extend>>` relationships to break down the complex interactions of specific Action Cards (e.g., Deal Breaker, Sly Deal, Rent).

### 2. Sequence Diagrams (Core Logic & Interaction)
These diagrams model the precise object interactions for our 5 most critical and high-risk game operations. They also serve as the blueprint for our subsequent JUnit testing phase.
* **`Fig3_Sequence_TurnStateTransition.svg`**: Shows the strict Turn State management (Draw -> Play -> Discard).
* **`Fig4_Sequence_CardDrawingLogic.svg`**: Details the interaction between the Model, Player hand, and Deck.
* **`Fig5_Sequence_StandardCardPlay.svg`**: Illustrates the standard MVC routing when a player plays a property or money card.
* **`Fig6_Sequence_AssetValidation.svg`**: Demonstrates the logic for validating and placing property sets.
* **`Fig7_Sequence_RentPaymentProcess.svg`**: Showcases the complex, multi-step asynchronous communication required for collecting rent from opponents.

### 3. Class Diagram (Clean Design & Architecture)
* **`Fig8_ClassDiagram_Architecture.svg`**: The complete system blueprint. This version provides a **deep-dive into the class hierarchy**, including the full inheritance tree for `ActionCard` and `PropertyCard` subclasses. It explicitly visualizes the interaction between the **8 design patterns** and the comprehensive method signatures required for the Phase-2 implementation.
* **`Fig9_ClassDiagram_Simplified.svg`**: A streamlined version focusing on the **Core MVC Architecture**. It highlights the relationships between major packages (`model`, `view`, `controller`, `state`) without the visual clutter of specific card attributes, making it ideal for a quick architectural overview.

---
*Note: In addition to the basic patterns explicitly required by the course, the project also plans to incorporate the State, Strategy, Command, and Factory patterns to handle complex turn transitions, AI decision-making, and card generation. The design concepts for these extended patterns are informed by the course-recommended textbook "Head First Design Patterns," representing the team's independent advanced learning beyond the baseline requirements.*