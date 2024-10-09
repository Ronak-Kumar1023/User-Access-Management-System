# User Access Management System

## Project Overview

This project implements a system that manages user access by limiting the number of active roles a person can hold. Each role grants access to specific resources or data, and the system ensures that only the last *k* roles used by a person remain active. If a new role is invoked and the user already has *k* active roles, the oldest role is replaced.

## Key Features

- **Role Limitation**: Ensures a user can only have *k* active roles at any given time.
- **Role Tracking**: Tracks the last role invocation message for each active role.
- **Eviction Policy**: When the limit of *k* roles is exceeded, the oldest role is removed to make space for a new one.

## Technologies Used

- **Python**: Core implementation of the role management system.
- **Data Structures**: Utilizes a dictionary and list to efficiently track roles and their invocation messages.

## Runtime Complexity

- **`get`**: Retrieves the last message for a given role in **O(N)** time, where *N* is the number of roles.
- **`set`**: Updates the role's message or adds a new role, with a time complexity of **O(N)**.
- **Space**: The space complexity is **O(k)**, where *k* is the maximum number of active roles.

## Conclusion

This project showcases a simple yet effective role management system based on a Least Recently Used (LRU) cache-like mechanism. It ensures compliance with the principle of least privilege by limiting active roles and keeping access control efficient.

## Links

https://medium.com/@ronak.kumar1023/unlocking-cybersecurity-skills-jp-morgan-chase-co-job-simulation-by-forage-eea0f78564f0
