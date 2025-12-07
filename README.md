### SRE
- In SRE, we mainly talk about the user experience of the services they are using.
- When a company is providing a service, it’s company's job to make sure their customers are getting the quality of service they expect from the company.
- For this, SRE mainly deals with Availability, uptime and latency of their service with respective to customer experience.
- **Availability:**
  - It means, how successfully users could be able to access or use the service.
  - To measure that there are few metrics like successful requests & failed requests.
    - `successful requests(%) = (number of successful requests/ Total number of requests) * 100`
    - `failed requests(%) = (number of failed requests/ Total number of requests) * 100`
- **Uptime:**
  - It means, the time/duration a system has been running without downtime.
  - `uptime = (Total time - downtime/total time) * 100`
  - Uptime and avialability can be related like,
    - High uptime does not guarantee high availability. A server can be "up" (100% Uptime), but if it's too slow or can't connect to the database, it has low Availability. This is the "Watermelon Effect" (green on the outside, red on the inside).
- **Latency:**
  - The delay between when a request is initiated and when the first byte of the response is returned.
  - It's measured in terms of Percentiles (p95, p99)
 
#### SLA, SLO, SLO:
- To achieve high avialability, high uptime & low latency. Companies work on SLA, SLO & SLI.
- **SLI:**
  - Service Level Indicator
  - A metric that measures the reliability of the service
  - It's the actual data you collect from the service.
  - Example: The number of successful requests per second, average response time, or the rate of successful probes

- **SLO:**
  - service level objective
  - It defines a target value for a particular metric over a set period of time
  - An SLO has three primary components: metric, target, and time window.
    - The metric is a measurable number, such as downtime or latency, while the target is the specific number you’re trying to achieve, for example, 99.9% downtime. The time window indicates how long it takes to measure the metric, ranging from a month to a year. 
  - The SLO is the specific goal that the service must meet in order to be in compliance with the SLA.
  - It is an internal target companies set to ensure the services deliver to meet customers’ expectations. These customer expectations are outlined in service level agreements (SLAs), agreements between company and the customer.
  - **the SLI’s value must always meet or exceed the value determined by the SLO.**
    - SLI = We measured availability. It is 99.2%.
    - SLO = Our target availability must be at least 99.9% 
- **SLA:**
  - service level agreement.
  - A formal contract or agreement with customers that specifies the terms of service.
  - if it fails to do so then some kind of penalty will be paid to the client.
    
- **Analogy:**
  - SLI = your weight, measured on scale (metric)
  - SLO = target weight you want to reach (goal)
  - SLA = what you promised to a trainer and incur penalty if you break 
