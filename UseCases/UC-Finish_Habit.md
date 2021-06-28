# Use-Case Specification: Finish Task

# 1. Buy Rewards

## 1.1 Brief Description
This use case allows users to finish a habit and earn coins as a reward.

## 1.2 Mockup



# 2. Flow of Events

## 2.1 Basic Flow

### Activity Diagram
![](PNGs/AC_Finish_Habit.png)

### .feature File

``` feature
Feature: Finish Habit
  This feature file tests the completion of Habits.
  It tests the completion of one habit and the completion of all habits of one type.
  It also checks if the coins are charged accordingly.

  Background:
    Given I am in Habits Tab

Scenario Outline: Finish Habit completely
And at least one habit is already created
When I hold click on habit <habit>
And I click on "FINISH"
And habit has exactly one point left to completely finish <finishedcount> <countCompl>
Then reward for one part and for completely finishing are added to balance <singelCoin> <rewardCoins> <balance>
And counter is raised by 1 <finishedcount>
And I go back to Habits Tab
Examples:
| habit | finishedcount | countCompl | singelCoin | rewardCoins | balance |
| Jogging | 9           | 10         | 15         | 25          | 5       |
| vacum   | 5           | 6          | 15         | 10          | 0       |
| cooking not ordering takeaway | 9 | 10 | 25     | 50          | 75      |

Scenario Outline: Finish Habit
And at least one habit is already created
When I hold click on habit <habit>
And I click on "FINISH"
And habit has more than one point left to completely finish <finishedcount> <countCompl>
Then reward for one part is added to balance <singelCoin> <balance>
And counter is raised by 1 <finishedcount>
And I go back to Habits Tab
Examples:
| habit | finishedcount | countCompl | singelCoin | balance |
| Jogging | 9           | 10         | 15         | 5       |
| vacum   | 2           | 6          | 15         | 0       |
| cooking not ordering takeaway | 6 | 10 | 25     | 75      |


    
```

## 2.2 Alternative Flows
n/a

# 3. Special Requirements
n/a

# 4. Preconditions


# 5. Postconditions

### 5.1 Buy Reward




# 6. Function Points
n/a
