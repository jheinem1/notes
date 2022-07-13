
- Two tests in parallel:
    - Test 1...
        - Middle layer with drivers and stubs
        - Top layer with stubs
        - Bottom layer with drivers
    - Test 2...
        - Top layer accessing middle layer (replaces drivers)
        - Bottom accessed by middle layer (bottom layer replaces stubs)