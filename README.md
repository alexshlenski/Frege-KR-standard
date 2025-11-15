# **RCI Interpreter — README**

## Overview

This document covers only RCI Interpreter. For general understanding of architecture and capabilities of Renyxa Cognitive Inventory please read the [RCI Whitepaper](https://github.com/alexshlenski/Renyxa-Cognitive-Inventory/blob/main/docs/RCI-whitepaper.pdf)

--------------------------------------------------------------------------------------------------------------------------

The **RCI Interpreter** is a deterministic analytical engine that operates fully inside an LLM session.  
It performs:

- Entity & alias unification

- Action & event extraction

- Timeline, causal chain, and dependency chain construction

- XREF-grounded reasoning

- Graph-ready output

The Interpreter does **not** hallucinate and does **not** use external knowledge unless asked.  
It works only from the **structured RCI profiles**  that you shouls upload to the LLM.

> **Important:**  
> **Only Kimi K2** (Moonshot AI) currently supports the prompt-controlled deterministic interpreter mode required by RCI.  
> The latest modifications of GPT-5.x refuse to run it.

---

# **Using RCI Interpreter in Kimi K2**

## **1. Start a fresh Kimi K2 chat**

Open [https://kimi.moonshot.cn](https://kimi.moonshot.cn) (or the enterprise endpoint).

Create a new session.  
Kimi must enter the chat with **no prior context**.

---

## **2. Upload the RCI Interpeter KB files**

2.1. Find the RCI interpreter prompt in /RCI-interpreter/RCI-interpreter-prompt.txt.

Upload the prompt file by drag-n-drop into Kimi dialog area. Kimi shall acnowledge the reception of the prompt file.

2.2. Find the ODS open-source spec file in /RCI-interpreter/ODS-open-source-spec.txt.

Upload the spec file by drag-n-drop into Kimi dialog area. Kimi shall acnowledge the reception of the prompt file.

2.3. Find the IFSN open-source spec file in /RCI-interpreter/IFSN-open-source-spec.txt.

Upload the spec file by drag-n-drop into Kimi dialog area. Kimi shall acnowledge the reception of the prompt file.

---------

## **3. Upload your RCI profile components**

RCI Interpreter accepts two component files:

### **Ontology Driven Scaffolding file**

The file name is <project-name>-ODS.json

Example: KENIA-ODS.json

Upload the ODS file by drag-n-drop into Kimi dialog area. Kimi shall acnowledge the reception of the ODS file.

---



### **Inference Free Semantic Notation file**

The file name is <project-name>-IFSN.txt

Example: KENIA-IFSN.txt

Upload the IFSN file by drag-n-drop into Kimi dialog area. Kimi shall acnowledge the reception of the IFSN file.

---

## **4. Start giving the Interpreter tasks and queries**

Once you uploaded the KB files and the RCI Profile components, you can issue any RCI analytical request.

### **Examples**

- Create a Mermaid timeline diagram for the main events for the entire time range

- List all financial transactions over $1,000,000 from December 2004 until January 2009, include sender, receiver, date and amount.

- List all government agencies referred in this text and their actions, including dates, locations and taskforce names when available.

- Create a brief dossier on every person suspected in terrorist activity. state their current location and status if available.



---

# **5. What NOT to do**

- Do **NOT** run the interpreter on GPT-5.x or any GPT transformers  
  (it will refuse to follow operational constraints)

- Do **NOT** mix profile sets

- Do **NOT** paste partial profiles

- Do **NOT** upload any files that RCI Interpreter is not expected. It will confuse the LLM and render it incapable to operate, rather than help.
  
  ---

# **Disclaimers**

Renyxa Cognitive Inventory is in a continuous development phase, therefore periodical changes in logic and operations are possible. We will try to keep the documentation up to date.

---

# **Support**

For questions, enhancements, or contribution proposals, please open an Issue or Contact the Project Owner.
