# datos_masivos
## Index
- [Homework 1](#Homework-1)
- [Homework 2](#IHomework-2)
- [Homework 3](#Homework-3)
- [Practice 1](#practice-1)
- [Practice 2](#practice-2)
- [Practice 3](#practice-3)
- [Practice 4](#practice-4)
- [Practice 5](#practice-5)
- [Practice 6](#practice-6)
- [Practice 7](#practice-7)
- [Evaluation](#evaluation)


## Homework 1
### Types of machine learning algorithms
1. Regression algorithms. They help us classify or predict values. An attempt will be made to compensate for the best
response from the smallest error.
<p align="center">
<img width="450"
src=https://i0.wp.com/www.aprendemachinelearning.com/wp-content/uploads/2017/11/icon_algoritmos_regresion.png?resize=300%2C150&ssl=1
raw=true">
</p>           

2. Bayesian algorithms
These types of algorithms by classification are included in Bayes' theorem and
they classify each value as independent of any other. What allows to predict
a class or category based on a given set of characteristics, using
probability
<p align="center">
<img width="450"
src=https://i0.wp.com/www.aprendemachinelearning.com/wp-content/uploads/2017/11/icon_algoritmo_bayesiano.png?resize=300%2C150&ssl=1
raw=true">
</p> 
         
3. Grouping algorithms
They are used in unsupervised learning, and are used to categorize data that is not
tagged, that is, data without specific categories or groups.
The algorithm works by searching for groups within the data, with the
number of groups represented by variable K.
<p align="center">
<img width="450"
src=https://i1.wp.com/www.aprendemachinelearning.com/wp-content/uploads/2017/11/icon_algoritmo_clustering.png?resize=300%2C150&ssl=1
raw=true">
</p> 
         
4. Decision tree algorithms
A decision tree is a tree structure similar to a flowchart that
uses a branching method to illustrate every possible outcome of a decision.
Each node within the tree represents a test on a specific variable, and
each branch is the result of that test.
<p align="center">
<img width="450"
src=https://i0.wp.com/www.aprendemachinelearning.com/wp-content/uploads/2017/11/icon_algoritmos_arbol_decision.png?resize=300%2C150&ssl=1
raw=true">
</p> 
         
5. Neural network algorithms.
Neural Networks mimic biological activation behavior and
interconnection between neurons to find non-linear solutions to problems
complex.
<p align="center">
<img width="450"
src=https://i2.wp.com/www.aprendemachinelearning.com/wp-content/uploads/2017/11/icon_red_neuronal.png?resize=300%2C150&ssl=1
raw=true">
</p> 
         
6. Dimension reduction algorithms
Dimension reduction reduces the number of variables considered for
find the exact information required.
Dimension reduction allows us to graph or simplify very complex models
that in their initial condition contained too many characteristics.
<p align="center">
<img width="450"
src=https://i0.wp.com/www.aprendemachinelearning.com/wp-content/uploads/2017/11/icon_reduccion_dimension.png?resize=300%2C150&ssl=1
raw=true">
</p> 
         
7. Deep Learning Algorithms
Deep learning algorithms execute data across multiple layers of
neural network algorithms, which pass to a simplified representation
from the data to the next layer.
Convolutional networks make a deep learning neural network
have the ability to recognize animals, humans and objects within images.

## Homework 2
### Vector Assembler.

VectorAssembleres a transformer that combines a given list of
columns in a single vector column. It is useful to combine
raw features and features generated by different feature transformers in a single feature vector, in order to train ML models such as logistic regression and decision trees. VectorAssemble accepts the following types of input columns: all numeric types, boolean type, and vector type. In each row, the values in the input columns will be concatenated into a vector in the specified order.
Examples
Suppose we have a data frame with the
id, hour, mobile, userFeatures, and clicked columns:

userFeatures is a vector column containing three functions of
user. We want to combine time, mobile user Features in a single vector
of features called features and use it to predict click no. Yes
you look VectorAssembler & # 39; s input columns
one hour, mobiley userFeaturesy the output column which features, then
From the transformation we should get the following data frame:

## Homework 3
### Pipeline
Pipeline architecture (based on filters) consists of transforming a data flow into a process comprised of several sequential phases, the input of each being the output of the previous one.
This architecture is very common in the development of programs for the command interpreter, since you can easily connect commands with pipes (pipe).
The pipe syntax, pipeline, allows connections to be clearly arranged in a sequence of multiple operations. It is a string syntax, so the operator% & gt; % takes the output ('the output') of a code statement and the conversion into the input ('the argument') of a new statement.

When describing the code we can think of it as "THEN".

The output (result) of the code to the left of%>% is argument of the function to the right.
<p align="center">
<img width="450"
src=https://rsanchezs.gitbooks.io/rprogramming/content/chapter9/pipeline.PNG
ssl=1
raw=true">
</p> 
         
### Confusion matrix
The confusion matrix of a problem of class n is an nxn matrix in which the rows are named according to the real classes and the columns, according to the classes predicted by the model. It is used to explicitly show when one class is confused with another. Therefore, it allows you to work separately with different types
of mistake.
For example, in a binary model that seeks to predict whether a mushroom is poisonous or not, based on certain physical characteristics of these we will consider the real classes p (positive = the mushroom is poisonous) and n (negative = the mushroom is edible), and
the classes predicted by the model, S (yes, it is poisonous), or N (no, it is edible).
In this way, the confusion matrix for this model has its rows labeled with the real classes, and its columns with those predicted by the model. It would look like this:
<p align="center">
<img width="450"
src=https://4.bp.blogspot.com/-v2ir_F1mlVU/WmCI1w8w7gI/AAAAAAAAH7M/jIWYNqCWoosjWeFCX6GucSl-DzPnlEOggCLcBGAs/s1600/matriz-confusion-sencilla.JPG
ssl=1
raw=true">
</p> 
         
Thus, the main diagonal contains the sum of all the predictions
correct (the model says "S" and hits, is poisonous, or says "N" and hits also, is
edible). The other diagonal reflects the classifier errors: false positives or
"True positives" (says that it is poisonous "S", but in reality it is not "n"), or false negatives or "false negatives" (says that it is edible "N", but in fact it is poisonous "p" ).

## Practice 1 
### Decision tree classifier

## Practice 2 
### Random Forest Classifier

// We import our libraries 
// $ example on $
import org.apache.spark.ml.Pipeline
import org.apache.spark.ml.classification. {RandomForestClassificationModel, RandomForestClassifier}
import org.apache.spark.ml.evaluation.MulticlassClassificationEvaluator
import org.apache.spark.ml.feature. {IndexToString, StringIndexer, VectorIndexer}
// $ example off $
import org.apache.spark.sql.SparkSession


  def main (): Unit = {
    val spark = SparkSession.builder.appName ("RandomForestClassifierExample"). getOrCreate ()

    // $ example on $
    // Load and parse the data file, turning it into a DataFrame.
    val data = spark.read.format ("libsvm"). load ("./ sample_libsvm_data.txt")

    // Index tags, metadata is added to the tag column.
    // Fits the entire dataset to include all the tags in the index.
    val labelIndexer = new StringIndexer (). setInputCol ("label"). setOutputCol ("indexedLabel"). fit (data)
    
    // Automatically identifies categorical features and indexes them.
    // The maxCategories are set so that entities with> 4 different values ​​are treated as continuous.
    val featureIndexer = new VectorIndexer (). setInputCol ("features"). setOutputCol ("indexedFeatures"). setMaxCategories (4) .fit (data)
    
    // Divide the data into training and test sets (30% for tests).
    val Array (trainingData, testData) = data.randomSplit (Array (0.7, 0.3))

    // Train a RandomForest model.
    val rf = new RandomForestClassifier (). setLabelCol ("indexedLabel"). setFeaturesCol ("indexedFeatures"). setNumTrees (10)

    // Convert indexed tags back to original tags.
    val labelConverter = new IndexToString (). setInputCol ("prediction"). setOutputCol ("predictedLabel"). setLabels (labelIndexer.labels)
    
    // Create a Pipeline with an array with the Indexers and RandomForest.
    val pipeline = new Pipeline (). setStages (Array (labelIndexer, featureIndexer, rf, labelConverter))

    // Train the model. This also runs the indexers.
    val model = pipeline.fit (trainingData)

    // Make predictions.
    val predictions = model.transform (testData)

    // Select example rows to display.
    predictions.select ("predictedLabel", "label", "features"). show (5)

    // Select (prediction, true label) and calculate test error.
    val evaluator = new MulticlassClassificationEvaluator (). setLabelCol ("indexedLabel"). setPredictionCol ("prediction"). setMetricName ("accuracy")
    val accuracy = evaluator.evaluate (predictions)
    println (s "Test Error = $ {(1.0 - accuracy)}")

    val rfModel = model.stages (2) .asInstanceOf [RandomForestClassificationModel]
    println (s "Learned classification forest model: \ n $ {rfModel.toDebugString}")
    // $ example off $

    spark.stop ()
  }
main ()

## Practice 3 
### Gradient Boosted Trees (GBTs)

// We import our libraries 
``
import org.apache.spark.ml.Pipeline
import org.apache.spark.ml.classification. {GBTClassificationModel, GBTClassifier}
import org.apache.spark.ml.evaluation.MulticlassClassificationEvaluator
import org.apache.spark.ml.feature. {IndexToString, StringIndexer, VectorIndexer}
``

// Spark session

``
import org.apache.spark.sql.SparkSession
import org.apache.log4j._
Logger.getLogger ("org"). SetLevel (Level.ERROR)
``

// We load our dataset from mlib

``
val data = spark.read.format ("libsvm"). load ("sample_libsvm_data.txt")
data.printSchema ()
``

// We index our labels to work them

``
val labelIndexer = new StringIndexer (). setInputCol ("label"). setOutputCol ("indexedLabel"). fit (data)
``

// Automatically indentifies categories and indexes them

``
val featureIndexer = new VectorIndexer (). setInputCol ("features"). setOutputCol ("indexedFeatures"). setMaxCategories (4) .fit (data)
``

// We divide our data set into training data and test or testing data 70% for training and% 30 for testing.

``
val Array (trainingData, testData) = data.randomSplit (Array (0.7, 0.3))
``

// We train our GBT model.

``
val gbt = new GBTClassifier (). setLabelCol ("indexedLabel"). setFeaturesCol ("indexedFeatures"). setMaxIter (10) .setFeatureSubsetStrategy ("auto")
``

// We turn our indexed tags into original tags

``
val labelConverter = new IndexToString (). setInputCol ("prediction"). setOutputCol ("predictedLabel"). setLabels (labelIndexer.labels)
``

// we join our gbt model our indexed labels through Pipeline

``
val pipeline = new Pipeline (). setStages (Array (labelIndexer, featureIndexer, gbt, labelConverter))
``

// We train our pipeline using training data and the fit function

``
val model = pipeline.fit (trainingData)
``

// We create our predictions transforming our data

``
val predictions = model.transform (testData)
``

// select some test columns and display them.

``
predictions.select ("predictedLabel", "label", "features"). show (5)
``

// We select our predictions and true labels as well as the margin of error obtained.

``
val evaluator = new MulticlassClassificationEvaluator (). setLabelCol ("indexedLabel"). setPredictionCol ("prediction"). setMetricName ("accuracy")
``

  // Evaluations and we get the percentage of the prediction
  
  ``
val accuracy = evaluator.evaluate (predictions)
println (s "Test Error = $ {1.0 - accuracy}")
``

// Print result of Trees using GBTs

``
val gbtModel = model.stages (2) .asInstanceOf [GBTClassificationModel]
println (s "Learned classification GBT model: \ n $ {gbtModel.toDebugString}")
``

## Practice 4 
### Multilayer-perceptron-classifier-

package org.apache.spark.examples.ml
//loading required packages and APIs
``
import org.apache.spark.ml.classification.MultilayerPerceptronClassifier
import org.apache.spark.ml.evaluation.MulticlassClassificationEvaluator
import org.apache.spark.sql.SparkSession
``
``
object MultilayerPerceptronClassifierExample
 {
   //create a Spark session
   // Where the class is as follows:
  def main (args: Array [String]): Unit = {
    val spark = SparkSession.builder.appName ("MultilayerPerceptronClassifierExample"). getOrCreate ()
    ``

    // load and analyze the dataset
    // Load the data stored in LIBSVM format as a DataFrame.
    // Spark store here is set to "/usr/local/spark-2.3.4-bin-hadoop2.6/data/mllib/s", but you should configure your path accordingly
    ``
   val data = spark.read.format ("libsvm"). load ("/ usr / local / spark-2.3.4-bin-hadoop2.6 / data / mllib / sample_multiclass_classification_data.txt")
   ``

    //preparing the training and test set
    // Prepare the train and the test set: training => 60%, test => 40% and seed => 12345L
    ``
    val splits = data.randomSplit (Array (0.6, 0.4), seed = 1234L)
    val train = splits (0)
    val test = splits (1)
    ``

    / * specify the layers for the neural network
    Specify the layers for the neural network as follows:
    input layer => size 4 (characteristics),
    two intermediate layers (i.e. hidden layer)
    of size 5 and 4 and output => size 3 (classes). * /
    ``
    val layers = Array [Int] (4, 5, 4, 3)
    ``

    //create the MultilayerPerceptronClassifier trainer and set its parameters
    ``
    val trainer = new MultilayerPerceptronClassifier (). setLayers (layers) .setBlockSize (128) .setSeed (1234L) .setMaxIter (100)
    ``
    
   / * Train the multilayer perceptron classification model using the estimator
    Train the multilayer perceptron classification model using the estimator above (i.e. trainer) * /
    val model = trainer.fit (train)
    
   // calculate the precision in the test set
   ``
    val result = model.transform (test)
    val predictionAndLabels = result.select ("prediction", "label")
    ``
    
  //evaluate the model for prediction performance
  ``
    val evaluator = new MulticlassClassificationEvaluator (). setMetricName ("accuracy")
    ``
    
  / * dummy adjustment if necessary
  if the classifier performance is low enough. One reason is that the Perceptron is very shallow
  the size of the data set is also smaller; therefore we must continue to try to deepen
   at least increasing the size of the hidden layers. * /

    println (s "Test set accuracy = $ {evaluator.evaluate (predictionAndLabels)}")
   
  //stop Spark session
  ``
    spark.stop ()
  }
}
``

## Practice 5 
### Linear Support Vector Machine

// We import libraries
``
package org.apache.spark.examples.ml
``

// Library for SVC
``
import org.apache.spark.ml.classification.LinearSVC
import org.apache.spark.sql.SparkSession
``

// Create session spark variable
``
val spark = SparkSession.builder.appName ("LinearSVCExample"). getOrCreate ()
``

// load the data from our file and add it to a variable to train
``
val training = spark.read.format ("libsvm"). load ("/ usr / local / spark-2.3.4-bin-hadoop2.6 / data / mllib / sample_libsvm_data.txt")
``

// create an object of type LinearSVC, Set the number of iterations to 10 with the setMaxIter method and Set the regularization parameter
``
val lsvc = new LinearSVC (). setMaxIter (10) .setRegParam (0.1)

``
// Fit the model
``
val lsvcModel = lsvc.fit (training)

``
// We print the coefficients of the vector and its interception
``
println (s "Coefficients: $ {lsvcModel.coefficients} Intercept: $ {lsvcModel.intercept}")
``
## Practice 6 
### One-vs-Rest classifier (a.k.a. One-vs-All)

## Practice 7 
### Naive Bayes

## Evaluation
