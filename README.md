# Optimizing an ML Pipeline in Azure

## Overview
This project is part of the Udacity Azure ML Nanodegree.
In this project, we build and optimize an Azure ML pipeline using the Python SDK and a provided Scikit-learn model.
This model is then compared to an Azure AutoML run.

## Summary
**The dataset contains details of people who opted into a marketing scheme. The objective is to predict who classified as in or out.**

**The best performing model was a VotingEnsemble from an AutoML experiment.**

## Scikit-learn Pipeline
**The pipeline was a SKLearn estimator architecture configured with HyperDriveConfig. The data was registered and introduced to SKLearn estimator as well as the script and compute target. The esimator was configured in in HyperDriveConfig along, with the parameter sampler set to Random and parameter around defaults(because of initial check at default levels were high), and the policy set to Bandit. The classification algorithm in the script used was a LogisticsRegressor to establish what the basal functionality of the HyperDive was.**

**The benefits of the RandomSampler is that it will very quickly give you multiple combinations of a unknown space of parameter and give you insight on where to focus next for example.**

**The benefits of a BanditPolicy is that it allows the experiment to terminate if after a specified number of runs if the the loss metric does contribute positively within a specified range of the Primary Metric.**

## AutoML
**The AutoML selected VotingEnsemble that mimicks a LightGBM model and generally uses imputed values for the majority of it important features even if they are floats. The feutures generally have to do with duration and thing corelated to how much time they have.** 

## Pipeline comparison
**The comparison between the models is like comparing apples and apple tarts, Where one is basal and the other with finess. The performance is similar where one has a faster performance from the AutoML. Their accuracy is similar around 0.9 Accuracy score with AutoML with about 0.04 increase. The pipeline archtecture of AutoML is simpler reminiscent of a stats.model. The two approaches are differ probably because AutoML is a measured approach and HyperDrive is allowed to be more random.** 

## Future work
**In to make a workflow which is reliable one would start with AutoML and use everything learnt to build a robust model from HyperDrive, or one more tolerant to drift.

## Proof of cluster clean up
By performing this command in Powershell: ``Clear-ClusterNode -Name node4 -Force``

## Christian License

Version 1.0

This work is licensed under the Christian License.

You are free to:
- Use the software for any purpose, including commercial purposes.
- Modify the software.
- Distribute the software.
- Sublicense the software.

Under the following terms:

1. You must acknowledge and honor the Christian God as the ultimate source of wisdom and creator of all things.

2. You must treat all individuals with kindness, compassion, and respect, following the teachings of Jesus Christ.

3. You must prioritize the well-being of others above personal gain or profit, following the principles of selflessness and service.

4. You must strive for honesty, integrity, and humility in all your interactions and endeavors.

5. You must use this software to promote love, peace, and justice in the world, reflecting the values of the Christian faith.

This license is inspired by the teachings of the King James Version (KJV) of the Bible. By using this software, you agree to abide by these terms and uphold the principles outlined above.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.SO HELP ME THAT THE WAY ALL MY WORK FEELS.

