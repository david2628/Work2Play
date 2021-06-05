# Use-Case Specification: Manipulate Task

# 1. Manipulate Task

## 1.1 Brief Description
This use case allows users to list all tasks, create, edit and delete tasks. So it describes the creation, reading, updating and deleting of Tasks (CRUD).




## 1.2 Mockups
### Task List
![](PNGs/Task-List.png)
### Create Task
![](PNGs/Task-Create.png)
### Edit/Delete Task
![](PNGs/Task-menu.png)



# 2. Flow of Events

## 2.1 Basic Flow

### Activity Diagram

![Activity Diagram](PNGs/AC_Add_Task.png)

### .feature File

[Task Feature File](https://github.com/rbnsch/Work2Play/blob/master/app/src/androidTest/assets/features/task.feature)

``` feature
Feature: Reward(CRUD)
  Background:
    Given I am in Rewards tab

  Scenario Outline: Create Reward
    When I click on "+" button
    And AddReward Screen is shown
    And I set name for reward <reward>
    And I set amount of coins as cost <cost>
    And I select repeatable or not <repeatable>
    And I clock "SAVE" button
    Then new reward is saved
    And I am moved back to rewards tab
    And new reward is shown
    Examples:
      | reward                  | cost  | repeatable |
      | watching a movie (2h30) | 50    | yes        |
      | watch one episode (1h)  | 20    | yes        |
      | Go to pub with Karl     | 85    | no         |

  Scenario Outline: Delete Reward
    And at least one reward is already created
    When I hold click on reward <reward>
    And I clock on "DELETE"
    Then reward is deleted
    Examples:
      | reward |
      | watching a movie (2h30) |
      | Go to pub with Karl     |
      | watch one episode (1h)  |
      |                         |

  Scenario Outline: Buy repeatable reward
    And at least one reward is already created
    When I click on reward <reward>
    And reward is repeatable <repeatable>
    And I have more coins than it costs  <balance> <cost>
    Then cost is substracted form balance
    And I go back to rewards tab
    Examples:
      | reward                  | cost  | repeatable | balance |
      | watching a movie (2h30) | 50    | yes        | 100     |
      | watch one episode (1h)  | 20    | yes        | 5       |
      | Go to pub with Karl     | 85    | no         | 90      |

  Scenario Outline: Buy non repeatable reward
    And at least one reward is already created
    When I click on reward <reward>
    And reward is not repeatable <repeatable>
    And I have more coins than it costs  <balance> <cost>
    Then cost is substracted form balance
    And reward is deleted
    And I go back to rewards tab
    Examples:
      | reward                  | cost  | repeatable | balance |
      | watching a movie (2h30) | 50    | yes        | 100     |
      | watch one episode (1h)  | 20    | yes        | 5       |
      | Go to pub with Karl     | 85    | no         | 90      |
```





# 3. Preconditions

The app must be open.

# 4. Postconditions

### 4.1 Create Task
After a task is created the user automatically returns to the Task List and the new task appers.
### 4.2 Edit Task
After editing a task the user automatically returns to the Task List and the updated task is shown.
### 4.3 Delete Task
After deleting a task the user automatically returns to the Task List and the deleted is removed.

# 5. Function Points
n/a
