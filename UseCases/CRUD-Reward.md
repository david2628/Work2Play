# Use-Case Specification: Manipulate Reward

# 1. Manipulate Reward

## 1.1 Brief Description
This use case allows users to list all rewards, create, edit and delete rewards. So it describes the creation, reading, updating and deleting of rewards (CRUD).



## 1.2 Mockups
### Reward List
![](PNGs/Reward-list.png)
### Create Rewards
![](PNGs/Reward-create.png)
### Edit/Delete Rewards
![](PNGs/Reward-menu.png)



# 2. Flow of Events
![](PNGs/diagramm-reward.png)

## 2.1 Basic Flow


### Activity Diagram

![](PNGs/AC_Delete_Reward.png)

### .feature File

[Rewards Feature File](https://github.com/rbnsch/Work2Play/blob/master/app/src/androidTest/assets/features/reward.feature)

``` feature
Feature: Reward(CRUD)
  This feature file is a CRUD and tests the creation and deletion of rewards.

  Background:
    Given I am in the Rewards Tab

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


```





## 2.2 Alternative Flows
n/a

# 3. Special Requirements
n/a

# 4. Preconditions

The app must be open.

# 5. Postconditions

### 5.1 Create Reward
After a reward is created the user automatically returns to the Reward List and the new reward appers.
### 5.2 Edit Reward
After editing a reward the user automatically returns to the reward List and the updated reward is shown.
### 5.3 Delete reward
After deleting a reward the user automatically returns to the reward List and the deleted is removed.

# 6. Function Points
n/a
