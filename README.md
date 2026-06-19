# HHCRSP-with-Complementary-Staffing-HPCS-

# Dataset Description

## Structure

There are three instance sizes: **small**, **medium**, and **large**. Instances for each size are stored in their corresponding folder. The general parameters for each size are named `s_params`, `m_params`, and `l_params` for small, medium, and large, respectively.

| Dataset                | Small          | Medium                          | Large                           |
|------------------------|----------------|---------------------------------|---------------------------------|
| Number of providers    | 2              | 2                               | 3                               |
| Number of days         | 1              | 5                               | 5                               |
| Number of patients     | {5, 10, 15}    | {25, 30, 40, 50, 75, 100}       | {25, 30, 40, 50, 75, 100}       |

---

## General Parameters

| Key | Description |
|-----|-------------|
| `C_n` | Cost of keeping temporary caregivers on-call per time unit, for skill levels 1 and 2 |
| `C_s` | Cost of sharing caregivers per time unit, for skill levels 1 and 2 |
| `C_t` | Cost of using temporary caregivers per time unit, for skill levels 1 and 2 |
| `T_c` | Travel cost per unit of Euclidean distance |
| `num_agency` | Number of providers (agencies) in collaboration |
| `num_days` | Number of days in the planning horizon |
| `num_scenarios` | Number of possible scenarios for daily demand |
| `num_skill` | Number of caregiver skill levels |
| `probabilities` | Probability of each demand scenario |
| `change_rate` | Change in the base number of daily patients per scenario, for patients requiring caregivers with skill levels 1 and 2 |
| `agency_sizes_patients` | Base number of patients requiring caregivers with skill levels 1 and 2, for each provider size (see `chosen_size`) |
| `agency_sizes_FC` | Number of full-time (permanent) caregivers with skill levels 1 and 2, for each provider size (see `chosen_size`) |
| `agency_sizes_TC` | Number of temporary caregiver candidates with skill levels 1 and 2, for each provider size (see `chosen_size`) |
| `B1` | β₁ |
| `B2` | β₂ |

---

## Instance-Level Keys

Listed in the order they appear in each instance file.

| Key | Description |
|-----|-------------|
| `Agency_FC` | Agency (provider) of each full-time (permanent) caregiver |
| `Agency_P` | Agency (provider) of each patient, per scenario-day |
| `Agency_TC` | Agency (provider) of each temporary caregiver candidate |
| `E` | Earliest time of the visit time window for each patient, per scenario-day |
| `FC_L` | Location of each full-time (permanent) caregiver |
| `FC_M` | Earliest availability time of each full-time (permanent) caregiver |
| `FC_N_Dummy` | Latest availability time of each full-time (permanent) caregiver |
| `FC_S` | Skill level of each full-time (permanent) caregiver |
| `L` | Latest time of the visit time window for each patient, per scenario-day |
| `P_L` | Location of each patient, per scenario-day |
| `R` | Required service level of each patient, per scenario-day |
| `TC_L` | Location of each temporary caregiver candidate |
| `TC_M` | Earliest availability time of each temporary caregiver candidate |
| `TC_N_Dummy` | Latest availability time of each temporary caregiver candidate |
| `TC_S` | Skill level of each temporary caregiver candidate |
| `chosen_size` | Size of each provider (agency), which determines `agency_sizes_patients`, `agency_sizes_FC`, and `agency_sizes_TC` |
| `n_FC` | Number of full-time (permanent) caregivers for each provider |
| `n_P` | Number of patients per scenario-day for each provider |
| `n_TC` | Number of temporary caregiver candidates for each provider |
| `service_duration` | Service duration of each patient, per scenario-day |
