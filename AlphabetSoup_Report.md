{\rtf1\ansi\ansicpg1252\cocoartf2639
\cocoatextscaling0\cocoaplatform0{\fonttbl\f0\fswiss\fcharset0 Helvetica;\f1\fmodern\fcharset0 Courier;\f2\froman\fcharset0 Times-Roman;
}
{\colortbl;\red255\green255\blue255;\red0\green0\blue0;\red255\green255\blue254;\red144\green1\blue18;
\red144\green1\blue18;\red255\green255\blue254;}
{\*\expandedcolortbl;;\cssrgb\c0\c0\c0;\cssrgb\c100000\c100000\c99608;\cssrgb\c63922\c8235\c8235;
\cssrgb\c63922\c8235\c8235;\cssrgb\c100000\c100000\c99608;}
\margl1440\margr1440\vieww11520\viewh8400\viewkind0
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural\partightenfactor0

\f0\fs24 \cf0 ## OVERVIEW\
The purpose of this analysis is to report Optimization on predictive model creation of best chance of success of the nonprofit foundation Alphabet Soup funding applicants. Quite verbose. \
\
## RESULTS\
*Data Preprocessing:\
	*Target for the model is \'91IS_SUCCESSFUL\'92 column\
	*Features for the model are \cf2 \cb3 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec4 'APPLICATION_TYPE'\strokec2 , \strokec4 'CLASSIFICATION'\strokec2 , \strokec4 'USE_CASE'\strokec2 , \strokec4 'AFFILIATION'\strokec2 , \strokec4 'ORGANIZATION\'92, 'ASK_AMT'\
	*Features dropped are \'92SPECIAL_CONSIDERATION\'92, \'92STATUS\'92, \'91INCOME_AMT\'92, \'91EIN\'92, \'92NAME\'92\
\
*Compiling, Training, and Evaluating the Model\
\
\pard\pardeftab720\partightenfactor0

\f1\fs26 \cf0 \cb1 \outl0\strokewidth0 Optimization Trial #1\
_________________________________________________________________\
 Layer (type)                Output Shape              Param #   \
=================================================================\
 dense_3 (Dense)             (None, 16)                704       \
                                                                 \
 dense_4 (Dense)             (None, 16)                272       \
                                                                 \
 dense_5 (Dense)             (None, 16)                272       \
                                                                 \
 dense_6 (Dense)             (None, 16)                272       \
                                                                 \
 dense_7 (Dense)             (None, 1)                 17        \
                                                                 \
=================================================================\
Total params: 1,537\
Trainable params: 1,537\
Non-trainable params: 0\
_________________________________________________________________\
\
RESULT:\
268/268 - 1s - loss: 0.5524 - accuracy: 0.7263 - 789ms/epoch - 3ms/step\
Loss: 0.552358865737915, Accuracy: 0.7262973785400391\
\
MODEL SAVED AS:\
\pard\pardeftab720\partightenfactor0

\fs28 \cf5 \cb6 AlphabetSoupCharity_Optimization_trial_1.h5\
\pard\pardeftab720\partightenfactor0

\fs26 \cf0 \cb1 _________________________________________________________________\
_________________________________________________________________\

\fs28 \
\pard\pardeftab720\partightenfactor0

\fs26 \cf0 \
Optimization Trial #2\
_________________________________________________________________\
 Layer (type)                Output Shape              Param #   \
=================================================================\
 dense_8 (Dense)             (None, 80)                3520      \
                                                                 \
 dense_9 (Dense)             (None, 40)                3240      \
                                                                 \
 dense_10 (Dense)            (None, 40)                1640      \
                                                                 \
 dense_11 (Dense)            (None, 40)                1640      \
                                                                 \
 dense_12 (Dense)            (None, 40)                1640      \
                                                                 \
 dense_13 (Dense)            (None, 1)                 41        \
                                                                 \
=================================================================\
Total params: 11,721\
Trainable params: 11,721\
Non-trainable params: 0\
_________________________________________________________________\
\pard\pardeftab720\partightenfactor0

\f2\fs24 \cf0 \
RESULT:\
\pard\pardeftab720\partightenfactor0

\f1\fs26 \cf0 268/268 - 0s - loss: 0.5549 - accuracy: 0.7230 - 463ms/epoch - 2ms/step\
Loss: 0.5549117922782898, Accuracy: 0.7230320572853088\
\pard\pardeftab720\partightenfactor0

\f2\fs24 \cf0 \
SAVED AS:\

\f1\fs28 \cf5 \cb6 AlphabetSoupCharity_Optimization_trial_2.h5
\f2\fs24 \cf0 \cb1 \
\pard\pardeftab720\partightenfactor0

\f1\fs26 \cf0 _________________________________________________________________\
_________________________________________________________________\
\pard\pardeftab720\partightenfactor0

\f2\fs24 \cf0 \
\
\pard\pardeftab720\partightenfactor0

\f1\fs26 \cf0 Model: "sequential_3"\
_________________________________________________________________\
 Layer (type)                Output Shape              Param #   \
=================================================================\
 dense_14 (Dense)            (None, 160)               7040      \
                                                                 \
 dense_15 (Dense)            (None, 80)                12880     \
                                                                 \
 dense_16 (Dense)            (None, 40)                3240      \
                                                                 \
 dense_17 (Dense)            (None, 1)                 41        \
                                                                 \
=================================================================\
Total params: 23,201\
Trainable params: 23,201\
Non-trainable params: 0\
_________________________________________________________________\
\pard\pardeftab720\partightenfactor0

\f2\fs24 \cf0 \
\pard\pardeftab720\partightenfactor0

\f1\fs26 \cf0 RESULT:\
268/268 - 0s - loss: 0.5539 - accuracy: 0.7249 - 468ms/epoch - 2ms/step\
Loss: 0.5539478063583374, Accuracy: 0.7248979806900024\
\
SAVED AS:\
\pard\pardeftab720\partightenfactor0

\fs28 \cf5 \cb6 AlphabetSoupCharity_Optimization_trial_3.h5\cf0 \cb1 \
\pard\pardeftab720\partightenfactor0

\fs26 \cf0 _________________________________________________________________\
_________________________________________________________________\
\
Model: "sequential_4"\
_________________________________________________________________\
 Layer (type)                Output Shape              Param #   \
=================================================================\
 dense_18 (Dense)            (None, 160)               7040      \
                                                                 \
 dense_19 (Dense)            (None, 80)                12880     \
                                                                 \
 dense_20 (Dense)            (None, 1)                 81        \
                                                                 \
=================================================================\
Total params: 20,001\
Trainable params: 20,001\
Non-trainable params: 0\
_________________________________________________________________\
\
RESULT:\
268/268 - 0s - loss: 0.5538 - accuracy: 0.7258 - 474ms/epoch - 2ms/step\
Loss: 0.5538213849067688, Accuracy: 0.7258309125900269\
\
SAVED AS:\
\pard\pardeftab720\partightenfactor0

\fs28 \cf5 \cb6 AlphabetSoupCharity_Optimization_trial_4.h5\cf0 \cb1 \
\pard\pardeftab720\partightenfactor0

\fs26 \cf0 _________________________________________________________________\
_________________________________________________________________\
Model: "sequential_15"\
_________________________________________________________________\
 Layer (type)                Output Shape              Param #   \
=================================================================\
 dense_56 (Dense)            (None, 320)               10240     \
                                                                 \
 dense_57 (Dense)            (None, 80)                25680     \
                                                                 \
 dense_58 (Dense)            (None, 20)                1620      \
                                                                 \
 dense_59 (Dense)            (None, 1)                 21        \
                                                                 \
=================================================================\
Total params: 37,561\
Trainable params: 37,561\
Non-trainable params: 0\
_________________________________________________________________\
\
RESULT:\
268/268 - 0s - loss: 0.5553 - accuracy: 0.7261 - 496ms/epoch - 2ms/step\
Loss: 0.5552871227264404, Accuracy: 0.726064145565033\
\
SAVED AS:\
\pard\pardeftab720\partightenfactor0

\fs28 \cf5 \cb6 AlphabetSoupCharity_Optimization_trial_5.h5\cf0 \cb1 \
\pard\pardeftab720\partightenfactor0

\fs26 \cf0 \
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural\partightenfactor0

\fs28 \cf0 \outl0\strokewidth0 \strokec2 *TARGET MODEL PERFORMANCE OF 75% FAILED!\
\
*Steps taken to increase model performance:\
	-Added hidden layers\
	-Removed hidden layers\
	-Increased Nodes\
	-Decreased Nodes\
	-Removed Features\
	-Reverted Removed Features\
	-Removed Different Features\
\
## SUMMARY\
Overall I was not able to attain target model performance. I achieved 72.61% Accuracy. \
\
I would recommend changing Activation parameters to Sigmoid for a better classification model, and increasing epochs count. \
	-Sigmoid Activation (logistic regression) is a great tool for Classification mainly because the log function has two distinct asymptotes. \
	-Increasing epochs would give the model more cycles for learning opportunities thus increasing model accuracy. \

\f0\fs24 \cf2 \
}