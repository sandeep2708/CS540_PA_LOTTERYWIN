# CS540_PA_LOTTERYWIN
PROGRAMMING_ASSIGNMENT_LOTTERY_WIN

# Classes

1. Process Class
Represents a process in the simulation.
Attributes:
process_id: A unique identifier for the process.
lottery_tickets: A list of lottery tickets assigned to the process.

2. Scheduler Class
Manages the lottery scheduling algorithm.

Attributes:

process_list: A list to store instances of the Process class.
total_lottery_tickets: The total number of lottery tickets in the system.
Methods:

add_process(process): Adds a process to the scheduler.
allocate_lottery_tickets(): Allocates lottery tickets to each process.
select_lottery_winner(): Randomly selects a process based on lottery tickets.

# Sample Usage

```python
lottery_scheduler = Scheduler()

process_a = Process("A", [1, 2, 3, 4, 5])
process_b = Process("B", [6, 7, 8])
process_c = Process("C", [9, 10])

lottery_scheduler.add_process(process_a)
lottery_scheduler.add_process(process_b)
lottery_scheduler.add_process(process_c)

lottery_scheduler.allocate_lottery_tickets()

winner_process = lottery_scheduler.select_lottery_winner()

if winner_process:
    print(f"Process {winner_process.process_id} wins the lottery!")
else:
    print("Processes are not available.")
