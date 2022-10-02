*Starting Kit for the RecoGym Challenge*
 
Prerequisites:
Python3
RecoGym: https://github.com/criteo-research/reco-gym
To install RecoGym, please, follow instructions provided in `README.md` file.

*Usage:*
(1) Create a python file. The file must be named as: `test_agent.py`.

(2) Implement a new Agent that confirms to the interface of the Agent used in RecoGym.

The new Agent must confirm to these conventions:
* The name of the Agent must be: `TestAgent`
* The name of the configurations (dictionary) must be: `test_agent_args`

(3) To launch the Agent and check how does it works in the evaluation environment, you shall execute the command:
 ```bash
python3 sim_test.py \
    --P 100 \
    --U 1000 \
    --Utest 2000 \
    --seed 42 \
    --K 5 \
    --F 50 \
    --sigma_omega 0.01 \
    --log_epsilon 0.005 \
    --entries_dir my_entries/challenge_entry.py
```

*Note:* _`sim_test.py`_ you shall find in RecoGym.

Where:
* _`P`_ -- number of products
* _`U`_ -- number of user to train
* _`Utest`_ -- number of users to test/evaluate
* _`seed`_ -- random number seed (used by RecoGym environment)
* _`K`_ -- latent factor
* _`F`_ -- number of product flips
* _`sigma_omega`_ -- used by RecoGym Env
* _`log_epsilon`_ -- used by RecoGym Env
* _`entries_dir`_ -- path to the directory when the Agent under the test is located

(4) Once you are happy with the Agent performance, you can submit the agent for evaluation to CodaLab system.

You need to put into a folder (e.g.: `test_dir`) these two files:
* `metadata` this file contains meta information and it should not be modified
* `test_agent.py`

Then, you shall execute this command to create a zip file to submit:
```bash
zip -r -j submission.zip test_dir
```

(5) Upload `submission.zip` to CodaLab.

*Example*
The example of the full Agent you shall find in this kit in `example` directory.
