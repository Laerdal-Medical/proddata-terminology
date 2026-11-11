# Data Model Terminology: approved terms

The 18 approved terms for simulation assessment data, word for word from the [Data Model Terminology page](https://laerdal-medical.github.io/proddata-terminology/). The terminology skill reads its definitions from this file. Change a definition only through the master copy, described in the README.

<!-- terms start -->

### Target participant

**Definition.** The intended individual, team, or unit, described by segment and experience level, for whom the learning outcomes are designed.

**Example.** First-year nursing students; an emergency department team training in situ.

**Also known as.** Participant or learner. INACSL’s standard term is “participant (also known as learner)”.

**Why this term.** “Participant” is role-based, so it works for an individual, a team or a unit. “Learner” implies one identified individual.

**What this term is not.** The identity of the people who take part in a session.

**Relates to.** Learning_outcome; Laerdal ID (the actual people who take part).

*Data product: Yes (`target_participant`)*

### Learning outcome

**Definition.** A specific, observable statement of what participants should demonstrate in a session as a result of training.

**Example.** “Uses closed-loop communication during a resuscitation.”

**Also known as.** Learning objective (widely used); training goal.

**Relates to.** Defines which expected actions are needed; creates the basis for scenarios; mapped to a competence / performance framework.

*Data product: Yes (`learning_outcome`)*

### Scenario

**Definition.** A structured representation of a real-world clinical situation, designed to provide the context for participants to practice and demonstrate expected actions in a safe environment.

**Example.** A progressing clinical case, such as a deteriorating asthma patient; a cardiac arrest team session that ends in return of circulation.

**Also known as.** Clinical scenario (SSH / INACSL Healthcare Simulation Dictionary); case or patient case.

*Data product: Yes (`scenario`)*

### Expected actions

**Definition.** The specific, observable actions participants are expected to perform to show a learning outcome has been achieved. Written for the scenario; an action can be marked critical when it is required.

**Example.** Repeats back an order in closed-loop communication; chest compressions at the target depth.

**Also known as.** Critical actions (AHA checklists, SSET, vrClinicals); expected behaviours (Creighton CCEI); performance or behavioural indicators.

**Relates to.** Lives in the assessment tool; derived from the learning outcome.

*Data product: Yes (`expected_actions`)*

### Assessment tool

**Definition.** A defined structure that sets out what participant performance is assessed against and how that performance is scored.

**Example.** Creighton CCEI, Lasater Clinical Judgment Rubric, TeamSTEPPS Team Performance Observation Tool.

**Also known as.** Assessment or evaluation instrument; rubric and checklist are types of assessment tool.

**Relates to.** May apply to a framework; contains the expected actions.

*Data product: Yes (`assessment_tool`)*

### Scenario assessment

**Definition.** Brings together the expected and critical actions and scoring logic used to assess performance in a specific scenario.

**Relates to.** Assessment tool, learning outcomes, expected actions and scenario; scored to give the assessment result.

*Data product: Yes (`scenario_assessment`)*

## Competence / performance framework

**Definition.** A published description of the competencies or performance expectations for participants, used as the standard which scenarios and assessments are built against.

**Example.** AACN Essentials and NCSBN CJMM (nursing); EPAs (medical education); TeamSTEPPS (team performance); CanMEDS; ACGME Milestones.

**Also known as.** Competence framework (also written competency framework).

**Relates to.** Learning outcomes, expected actions and assessment tools are mapped to it.

*Data product: Yes (`competence_performance_framework`)*

### Modality

**Definition.** The format through which an educational or quality improvement activity is delivered.

**Example.** Manikin-based simulation, virtual reality.

**Also known as.** Simulation method or type.

**Relates to.** Training session.

*Data product: Yes (`modality`)*

### Training session

**Definition.** A single run of a learning activity involving one or more participants, with a defined start and end (runs that time out or are abandoned also count). A run is one attempt. Repeating the activity or starting over begins a new training session, while pausing and resuming stay inside the same training session.

**Example.** A YouSim conversation with a virtual patient; an abandoned chest pain scenario on SimMan with several participants.

**Also known as.** Simulation session; scenario run; session.

**What this term is not.** A user logging into a platform without taking part in a learning activity, e.g. creating a course on SimCapture or purchasing a product on Laerdal Connect.

**Relates to.** Scenario; modality; output; assessment result.

*Data product: Yes (`training_session`)*

### Session output

**Definition.** Everything captured from a training session: transcript, audio or video, event log, facilitator annotations and completed forms.

**Example.** The full transcript of a conversation with a virtual patient; the event log from a manikin session.

**Relates to.** Evidence is observed in or derived from it; the assessment result is worked out from it.

*Data product: No · Operational data: Yes*

### Session evidence

**Definition.** Anything observed in, or derived from, a session output that shows whether an expected action was performed, or any unexpected action relevant to performance.

**Example.** The expected action is “calls for help”. The recording shows the participant saying “Please call the emergency team” at 01:20. That moment is the evidence. If the event log shows a different drug given than the scenario planned.

**Relates to.** Observed in or derived from the output, by comparing it with the expected actions in the assessment tool; the assessment result is derived from it.

*Data product: No · Operational data: Yes*

### Assessment result

**Definition.** The completed assessment tool, showing whether each expected action was achieved.

**Example.** A completed Creighton evaluation with a score of 19 out of 20.

**Also known as.** SimCapture calls the completed record an “evaluation”. It can also be a score or a rating.

**Relates to.** Derived from evidence; forms the basis for feedback.

*Data product: Yes (`assessment_result`)*


### Prebrief

**Definition.** The orientation given to participants before a session begins. It sets out the learning outcomes and expectations, explains the environment, equipment and roles, and creates the psychological safety for the participants to engage and learn.

*Data product: No · Operational data: Yes*

### Debrief

**Definition.** A facilitated conversation in which participants reflect on an experience, to explore and understand the relationships between events, actions, thoughts, feelings and performance outcomes. It is a guided dialogue that uncovers the assumptions behind participants’ actions, so they can be understood and, where needed, corrected.

*Data product: No · Operational data: Yes*

### Assessment

**Definition.** The systematic process of gathering, interpreting and using information about participant performance to inform teaching, enhance learning and, ultimately, improve patient outcomes. Not merely a measurement of knowledge or skills but a dynamic, evidence-informed practice. Its result is the basis for feedback.

**Formative assessment.** Carried out during or after a learning experience to show progress, guide reflection and support mastery learning. Informs formative feedback.

**Summative assessment.** Used to judge competence against defined standards, often in high-stakes or credentialing contexts. Informs summative feedback.

*Data product: No · Operational data: No*

### Feedback

**Definition.** Information and guidance given to participants about their performance or progress, based on an assessment, to improve their actions or behaviour. It can be on a screen, on paper, in conversation, live or afterwards. To be useful it should be clear, specific, timely and encourage active participation.

Feedback is based on an assessment but is not one.

#### Formative feedback

**Definition.** Ongoing guidance that helps participants see their strengths and areas for growth, given during or after a learning experience.

*Data product: No · Operational data: No*

#### Summative feedback

**Definition.** Feedback that states how performance measured up at the end of a learning process, based on the assessment result, and points to next steps.

*Data product: No · Operational data: No*

<!-- terms end -->
