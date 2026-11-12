# Word list

The terminology skill reads this list on every run to decide which code names to flag. It looks at code names only: variables, functions, classes, object keys, database fields and file names. It never renames anything. It flags the name and suggests the approved one, and the builder decides.

A name missing from this list is never flagged. To flag a new name, add a row. To stop flagging one, delete its row.

Every suggested name comes from a term in [terms.md](terms.md): the term's data product name where it has one, otherwise the term name in snake_case.

## Suggest

The skill flags the name and offers the approved name.

| Look for in code | Suggest |
|---|---|
| `target_learner` | `target_participant` |
| `learning_objective`, `training_goal` | `learning_outcome` |
| `performance_indicator`, `behavioural_indicator`, `behavioral_indicator`, `expected_behaviour`, `expected_behavior` | `expected_action` for one, `expected_actions` for a list |
| `assessment_instrument`, `evaluation_instrument`, `evaluation_tool` | `assessment_tool` |
| `scenario_evaluation`, `scenario_checklist` | `scenario_assessment` |
| `simulation_method` | `modality` |
| `simulation_session`, `sim_session`, `scenario_run` | `training_session` |
| `evaluation_result`, `completed_evaluation` | `assessment_result` |

## Ask

The name can mean two things. The skill asks the builder the question and suggests a name only after the answer.

| Look for in code | Question to ask | Suggest, by answer |
|---|---|---|
| `attempt` | Is this one run of the activity, or the record saved after the run? | The run: `training_session`. The saved record: `session_output`. |
| `session` | Is this one run of a learning activity, or a login or connection? | A run: `training_session`. A login: nothing. |
| `evaluation` | Is this the completed and scored form, the blank form, or the process? | Completed: `assessment_result`. Blank: `assessment_tool`. Process: `assessment`. |
| `simulation_type` | Is this a delivery format, such as manikin or VR, or a kind of scenario? | A format: `modality`. A kind of scenario: nothing. |
| `patient_case`, `clinical_case` | Does this hold the whole scenario, or only the patient's story inside it? | The whole scenario: `scenario`. The story: nothing. |
| `session_data`, `session_record` | Does this hold everything captured from one run? | Yes: `session_output`. No: nothing. |

## Never flag

These names look like variants but are fine. The skill leaves them alone.

- **People:** `learner`, `participant`, `learner_id`, `participant_id`, `user_id`, `student_id`, `laerdal_id`. The team has not agreed role names yet.
- **Everyday code words:** `case`, `output`, `result`, `score`, `rating`, `grade`, `action`, `indicator`, `instrument`, `framework`, `goal`, `objective`, `outcome`, `run`, `type`, `mode`, `evaluate`, `eval`, `feedback`, `max_attempts`, `attempt_count`, `retry`.
- **Parts of a session output:** `transcript`, `event_log`, `session_events`, `recording`.
- **Different concepts:** `critical_action` and `is_critical` (a critical action is one kind of expected action), `reflection` (a participant's own answers, not a debrief).
- **Spelling variants of approved terms:** `preBrief`, `pre_brief`, `debriefing`.
- **Approved names and tool types:** `rubric`, `checklist`, `clinical_scenario`.
