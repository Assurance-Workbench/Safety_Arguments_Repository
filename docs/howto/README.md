
## How to Add a Safety Argument to the Repository

1. Optionally, clone the repository on your local machine.

2. Create a new branch to the repository either locally or directly on github. In this branch, you will add your argument [[see here]](./figures/create_branch.gif).

3. In the newly created branch, add a folder with a _Readme.md_ file. The folder should be under the _arguments_ parent folder. For example,  _arguments/myargument_. After creating the new folder, commit the changes  [[see here]](.figures/create_folder.gif).

4. Create a new codespace in the github cloud. An IDE for VSCode will open with the _Safety Arguments Repository_ project. Alternatively, if you are working on  on your local machine, open the project in VSCode IDE. There, you will also find your newly created folder. Once you created a codespace, you can access it whenever you want [[see here]](./figures/create_codespace.gif).

5. Install the Goal Structuring Notation extension in the codespace/in your IDE
[[see here]](./figures/add_extension.gif).

6. Add a new gsn file to your folder and specify your argument in the gsn file. Comprehensive examples about the syntax are available in this [repository](https://github.com/Assurance-Workbench/Demo_Safety_Case).
  - Define a new goal structure, at the begining of the file, using:    
    ```
      goal_structure <goal_structure_name>;
    ```
  - Define the goal structure elements, using: 
    ```
      <element_type> <element_name> {
        description: "<element description>";
      }
    ```
    For example:
    ```
      goal G1 {
        description: "Our autonomous driver is safe enough to deploy";
      }
    ```
  - Specify relationships between the goal structure elements [[see here]](./figures/create_argument.gif), adding to an element the following: 
    ```
      supported_by: <name_of_the_supporting_element>;
    ``` 
    or 
    ```
      in_context_of: <name_of_the_context_element>;
    ``` 
    For example:
     ```
      goal G1 {
        description: "Our autonomous driver is safe enough to deploy";
        supported_by: S1;
      }
     ```

  - Reference elements in other diagrams from elements in the current diagram via the _away_ construct [[see here]](./figures/create_away_elements.gif). For example: 
    ```
    strategy Str1_1 {
      description: "Description";
      supported_by: G2_1_away;
    }

    goal G2_1_away {
      description: "Description";
      away: G2_1;
    }
    ```

7. Open the diagram [[see here]](./figures/open_diagram.gif).

8. Commit and push the changes to your branch [[see here]](./figures/git_commit.gif).

9. Edit your argument as many times as you want. Don't forget to commit your changes :wink: !
10. Before publishing your argument to the Safety Arguments Repository, edit the `Readme.md` file in the folder of the argument. In this file, you can add a bit of information about the argument you specified. For example: where it was first published, its main goal, or how and when it could be used in a safety case. You can take inspiration from the Readme files of other arguments in the repository.
11. Enhance the index in the main [README.md](./../../README.md).
12. Create a `Pull Request`. Your contribution will be then reviewed and will either be merged into the main branch, or you will receive some recommendation for improvement.

