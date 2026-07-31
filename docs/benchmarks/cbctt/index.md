# Curriculum-Based Course Timetabling (CB-CTT)

## :material-file-document-outline: Description
A Collection of CB-CTT instances from different competitions, research projects and real-world examples.  
Difficulty can be adjusted through the problem formulations UD1-UD5.
The table below shows which constraints and which weights correspond to each
problem formulation.

| Constraint           | UD1 | UD2 | UD3 | UD4 | UD5 |
| -------------------- | --- | --- | --- | --- | --- |
| H1 Lectures          |   H |   H |   H |   H |   H |
| H2 Conflicts         |   H |   H |   H |   H |   H |
| H3 RoomOccupancy     |   H |   H |   H |   H |   H |
| H4 Availability      |   H |   H |   H |   H |   H |
| S1 RoomCapacity      |   1 |   1 |   1 |   1 |   1 |
| S2 MinWorkingDays    |   5 |   5 |   - |   1 |   5 |
| S3 IsolatedLectures  |   1 |   2 |   - |   - |   1 |
| S4 Windows           |   - |   - |   4 |   1 |   2 |
| S5 RoomStability     |   - |   1 |   - |   - |   - |
| S6 StudentMinMaxLoad |   - |   - |   2 |   1 |   2 |
| S7 TravelDistance    |   - |   - |   - |   - |   2 |
| S8 RoomSuitability   |   - |   - |   3 |   H |   - |
| S9 DoubleLectures    |   - |   - |   - |   1 |   - |

## :material-play-circle-outline: Usage

Example call:
```bash
clingo teaspoon.lp <formulation.lp> <instance.lp>
```

## :material-information-outline: Metadata
### :material-cog-outline: Technical Details
* **Type:** Optimization, Multi-shot
* **Format:** clingo
* **Tested With:** clingo 5.8.0

### :material-chart-bar: Instances
* **Details:**  
61 instances of varying size and difficulty. Both artificial and real-world instances are included.

### :material-lock-outline: Data & Access (Confidentiality)
* **Status:** Public
* **License:** MIT
* **Sensitivity:** None

### :material-book-open-variant: Source & Literature
* **Repository/ZIP:**  
On the institute cluster: `/mnt/beegfs/home/toschmidt/benchmarks/cb-ctt`
* **Reference:**  
Banbara, M., Inoue, K., Kaufmann, B. et al. teaspoon: solving the curriculum-based course timetabling problems with answer set programming. Ann Oper Res 275, 3–37 (2019).
doi:10.1007/s10479-018-2757-7

### :material-card-account-mail-outline: Contact
* **Name:** Tom Schmidt
* **Email:** tom.schmidt@uni-potsdam.de

### :material-lightbulb-outline: Miscellaneous
* **Complexity:** NP-hard

## :material-download-outline: Download

In the future you will be able to download the benchmark set here.
