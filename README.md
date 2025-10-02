# CS-370-Module-8
Briefly explain the work that you did on this project: What code were you given? What code did you create yourself?

The code that was given was the TreasureMaze environment (with reset, observe, act, valid_actions, and free_cells), the GameExperience replay buffer (with remember and get_data), a compiled Keras model, a global epsilon, a completion_check() helper, and a pseudocode skeleton for qtrain. And the code needed to complete this that I made was I made a full training loop inside qtrain: seeding each epoch from a random free cell, running an epsilon-greedy policy over valid_actions, calling model.predict() for exploitation, storing transitions in replay, sampling mini-batches via experience.get_data(), training with model.fit(), evaluating loss, and tracking performance with win_history, a sliding-window win_rate, and early-stopping when the agent sustained wins and passed completion_check. It also gave a print out of loss, episodes, win rate, and elapsed time. 

What do computer scientists do and why does it matter?

Computer scientists turn messy, real-world problems into precise representations, pick or design algorithms, and then test, measure, and iterate. The reason this matters is because those choices ripple into products that people rely on recommendations, navigation, safety systems, and even study aids.

How do I approach a problem as a computer scientist?

You approach problems as a computer scientists by formalizing the task, select data structures and abstractions, implement the smallest end-to-end version, instrument it with metrics, and iterate. 

What are my ethical responsibilities to the end user and the organization?

The ethical responsibilites to the end user is I should prioritize safety, privacy, and transparency—log decisions, avoid hidden manipulation, and document limitations so people know when the model might fail. And for the organization it is that I should write reproducible, testable code, handle data responsibly and least-privilege access and retention limits, and communicate risks early. 
