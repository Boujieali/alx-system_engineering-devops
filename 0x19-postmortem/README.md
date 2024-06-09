INCIDENT REPORT


Incident Summary

Duration of Outage: January 15, 2024, 9:30 AM - 12:45 PM UTC
Impact: The AgriConnect platform experienced a complete service disruption, preventing farmers from posting crop information and buyers from accessing listings. This affected around 1,200 users during the outage period.
Root Cause: The outage was traced back to a malfunction in the caching layer, where a recent update caused data corruption, leading to repeated crashes of the server handling requests.

Timeline

9:15 AM: New update deployed to the caching layer.
9:30 AM: Users began reporting issues accessing crop listings and submitting posts.
9:40 AM: Automated monitoring alerted the engineering team to a significant spike in server errors.
9:45 AM: Initial investigation initiated by the on-call engineer.
10:00 AM: Error logs pointed to data corruption in the caching layer.
10:30 AM: Misleading path: Network team investigated potential connectivity issues, but no problems were found.
11:00 AM: Root cause isolated to the caching layer after deeper log analysis.
11:15 AM: Decision made to disable the caching layer temporarily.
11:30 AM: Incident escalated to the platform's lead architect for further resolution.
12:00 PM: Caching layer disabled, servers restarted, and initial functionality restored.
12:45 PM: Full platform functionality confirmed, incident resolved.

Root Cause and Resolution

Root Cause: The incident stemmed from a malfunction introduced in a recent update to the caching layer. The update inadvertently caused data corruption, which led to repeated crashes of the server responsible for handling user requests. This disrupted the entire service, preventing users from accessing or posting crop information.
Resolution: To resolve the issue, the caching layer was temporarily disabled, and the server was restarted to restore basic functionality. Further analysis and debugging led to identifying and fixing the specific bug in the update that caused the data corruption. After verifying the fix, the caching layer was carefully re-enabled, ensuring stable operation.

Corrective and Preventative Measures
Improvements and Fixes

Update Validation: Enhance the process of validating updates to critical components like the caching layer to prevent similar malfunctions.
Robust Monitoring: Implement more detailed monitoring of the caching layer to detect and diagnose issues swiftly.
Extended Testing: Broaden testing protocols to include more scenarios, particularly focusing on data integrity and error handling in the caching layer.

Tasks

Fix Caching Layer Update: Correct the bug causing data corruption and verify stability.
Improve Update Validation: Establish stricter validation processes for updates, including additional peer reviews and automated tests.
Enhance Monitoring: Implement detailed monitoring for the caching layer to catch issues early.
Expand Testing Scenarios: Develop and execute more comprehensive tests to cover edge cases and data integrity checks.
Conduct Incident Review: Hold a team review session to discuss the incident and refine response protocols.

Conclusion

This incident underscored the critical need for robust update validation and monitoring mechanisms. The swift and coordinated response of the AgriConnect team ensured that the issue was resolved in a timely manner, minimising the impact on users. Moving forward, the team is committed to enhancing processes and protocols to prevent such incidents, ensuring the platform's reliability and the trust of its users.


