# Project Name
Timothy Seo
Date of Test Readiness Review

- system overview/test overview
- stakeholders
- test purpose
- success criteria
- system configuration
- ground test results
- test execution
- risks


# system overview


# stakeholders


**Error:** Gemini HTTP 429: {
  "error": {
    "code": 429,
    "message": "You exceeded your current quota, please check your plan and billing details. For more information on this error, head to: https://ai.google.dev/gemini-api/docs/rate-limits. To monitor your current usage, head to: https://ai.dev/rate-limit. ",
    "status": "RESOURCE_EXHAUSTED",
    "details": [
      {
        "@type": "type.googleapis.com/google.rpc.Help",
        "links": [
          {
            "description": "Learn more about Gemini API quotas",
            "url": "https://ai.google.dev/gemini-api/docs/rate-limits"
          }
        ]
      }
    ]
  }
}


***


***
> [!info] **Gemini Query** (2026-10-14T22:06:02.512Z)
> **Question:**
> how to setup api
> 
> **Model:** gemini-flash-latest
> 
>

***


***
> [!info] **Gemini Query** (2026-10-14T22:05:43.625Z)
> **Question:**
> how to setup api?
> 
> **Model:** gemini-flash-latest
> 
>


***


***
> [!info] **Gemini Query** (2026-10-14T22:04:12.227Z)
> **Question:**
> how to setup api
> 
> **Model:** gemini-flash-latest
> 
>

# test purpose
The purpose of this test is to validate the MATLAB model of the rocket. 

# success criteria
There are three main criteria to determine success of this test. First is accuracy of the model to the data collected from the test. In order to quantitatively measure the accuracy of the model, we will use coefficient of determination for each respective phases of the rocket. R-squared value of 0.75 or above would be considered successful. Second criteria for success 

# system configuration
## hardware
version numbers and configurations, masses, etc. 

## software
version numbers

## documentation
version numbers and approval name/date



# ground test results


# test execution
Cover the following: 
- flow—overview and point to separate procedures document
- personnel
- facilities
- resources
- documentation

# risks
Risks characterized IAW NATO S&T Flight Test Safety and Risk Management dated 2021-01: [https://apps.dtic.mil/sti/trecms/pdf/AD1183573.pdf](https://apps.dtic.mil/sti/trecms/pdf/AD1183573.pdf#page=41).
## severity

| catastrophic             | critical                      | marginal                     | negligible                    |
| ------------------------ | ----------------------------- | ---------------------------- | ----------------------------- |
| loss of life or aircraft | major damage or severe injury | minor damage or minor injury | less than minor damage/injury |
## probability

| frequent                          | probable                    | occasional                            | remote                             | improbable                              | incredible                                   |
| --------------------------------- | --------------------------- | ------------------------------------- | ---------------------------------- | --------------------------------------- | -------------------------------------------- |
| will occur often during the trial | will occur during the trial | could possibly occur during the trial | unlikely to occur during the trial | very unlikely to occur during the trial | extremely unlikely to occur during the trial |
| numerous                          | p=1                         | 1>p≥$10^{-2}$                         | $10^{-2}$>p≥$10^{-4}$              | $10^{-4}$>p≥$10^{-6}$                   | p<$10^{-6}$                                  |

## risk matrix
![](../../notes/assets/risk_matrix.png)

### risk 1: bystander injury
Errant rocket strikes and injures bystander at high speed

Risk: Medium

Mitigations
- bystanders stand at least 50 m from launch pad
- bystanders pay attention during all launch activities
- test conductor(s) call out loud countdown/launch announcements

Residual Risk: Low

|            | catastrophic | critical | marginal | negligible |
| ---------- | ------------ | -------- | -------- | ---------- |
| frequent   |              |          |          |            |
| probable   |              |          |          |            |
| occasional |              |          |          |            |
| remote     |              |          | before   |            |
| improbable |              |          | after    |            |
| incredible |              |          |          |            |

### risk 2: XXX

