# PAA17_1
This repo contains the files for PAA17.1

By Uday Kemburu


################################################################################
#                          1. BUSINESS UNDERSTANDING                             #
################################################################################

#------------------------------------------------------------------------------#
# 1.1 OBJECTIVE                                                                 #
#------------------------------------------------------------------------------#
# To optimize the bank's direct marketing campaigns (phone calls) by predicting 
# whether a client will subscribe to a term deposit. This will help the bank to 
# identify the most promising clients to contact, thereby reducing marketing costs 
# and increasing conversion rates.

#------------------------------------------------------------------------------#
# 1.2 BUSINESS SUCCESS CRITERIA                                                 #
#------------------------------------------------------------------------------#
# - Increase the success rate of term deposit subscriptions
# - Reduce the number of unnecessary phone calls
# - Achieve a minimum prediction accuracy of 85%
# - Reduce marketing costs by targeting the most likely customers

#------------------------------------------------------------------------------#
# 1.3 ASSESS SITUATION                                                         #
#------------------------------------------------------------------------------#

# a) Resources
# -----------
# - Dataset with 41,188 client records
# - 20 features including client demographics, campaign information, and economic 
#   indicators
# - Historical data from previous marketing campaigns

# b) Constraints
# -------------
# - Data privacy regulations 
# - Budget limitations for marketing campaigns
# - Resource constraints for making phone calls

# c) Risks
# --------
# - Missing important features that could influence customer decisions
# - Overfitting to historical data

#------------------------------------------------------------------------------#
# 1.4 DATA MINING GOALS                                                        #
#------------------------------------------------------------------------------#
# - Identify key characteristics of clients likely to subscribe
# - Determine optimal timing for contact

#------------------------------------------------------------------------------#
# 1.5 PROJECT PLAN                                                             #
#------------------------------------------------------------------------------#
# Phase 1: Data Understanding
# Phase 2: Data Preparation
# Phase 3: Modeling
# Phase 4: Evaluation
# Phase 5: Deployment

#------------------------------------------------------------------------------#
# KEY PERFORMANCE INDICATORS (KPIs)                                            #
#------------------------------------------------------------------------------#

# 1. Model Performance
# -------------------
# - Prediction accuracy

# 2. Business Impact
# -----------------
# - Conversion rate improvement
# - Campaign efficiency metrics
# - Return on marketing investment (ROMI)





#------------------------------------------------------------------------------#
#                         MODEL COMPARISON SUMMARY                              #
#------------------------------------------------------------------------------#

# 1. Model Performance Overview:
#    SVM achieved highest training accuracy (91.05%) but with longest training 
#    time (995s). Logistic Regression and Decision Tree showed similar test 
#    accuracy (89.71% and 89.62%) with much faster training times.

# 2. Efficiency Analysis:
#    Logistic Regression (L2 penalty, C=0.01) emerged as most efficient model:
#    - Competitive test accuracy: 89.71%
#    - Fastest training time: 3.87s
#    - Most practical for deployment

# 3. KNN Performance:
#    - Configuration: 9 neighbors, Manhattan distance
#    - Good training accuracy: 90.71%
#    - Lower test accuracy: 89.18%
#    - Moderate training time: 30.24s
#    - Shows signs of potential overfitting

# 4. Decision Tree Insights:
#    - Configuration: max_depth=5, minimal leaf/split parameters
#    - Balanced performance (train: 90.45%, test: 89.62%)
#    - Quick training time: 6.18s
#    - Good balance of performance and interpretability

# 5. Key Takeaway:
#    Small test accuracy range (89.18% - 89.71%) suggests simpler models 
#    (like Logistic Regression) are preferable due to faster training times 
#    and comparable performance to complex models.

#------------------------------------------------------------------------------#


#------------------------------------------------------------------------------#
#                         FEATURE SELECTION SUMMARY                             #
#------------------------------------------------------------------------------#

# Key Findings from Feature Selection:
# - Successfully reduced feature set from 20 to 8 features (60% reduction)
# - Maintained high model performance (test accuracy: 89.44%)

# Selected Features Analysis:
# 1. Customer Demographics:
#    - marital status and education level emerged as key predictors
#    - demonstrates importance of client's personal background

# 2. Campaign-Related Features:
#    - campaign (number of contacts)
#    - pdays (days since last contact)
#    - poutcome (previous campaign outcome)
#    - day_of_week (timing of contact)
#    - shows significance of campaign execution strategy

# 3. Economic Indicators:
#    - emp.var.rate (employment variation rate)
#    - nr.employed (number of employees)
#    - indicates strong influence of economic conditions

# Performance Impact:
# - Train Accuracy: 90.10% 
# - Test Accuracy:  89.44%
# - Small gap between train and test accuracy suggests good generalization
# - Model maintains robust performance with reduced feature set

# Business Implications:
# - More efficient model with fewer input requirements
# - Focused data collection on most impactful features
# - Simplified deployment and maintenance
#------------------------------------------------------------------------------#

#------------------------------------------------------------------------------#
#                    NEXT STEPS AND RECOMMENDATIONS                            #
#------------------------------------------------------------------------------#

# 1. Model Implementation:
#    - Deploy Logistic Regression as primary model due to:
#      * Best balance of accuracy (89.71%) and training time (3.87s)
#      * Simple implementation and interpretation
#      * Good performance with reduced feature set

# 2. Feature Engineering:
#    - Focus on the 8 selected features identified
#    - Develop time related features from day_of_week and campaign data

# 3. Business Process Integration:
#    - Update data collection to prioritize identified key features

# 4. Future Improvements:
#    - Regular model retraining with new campaign data

# LINK to the notebook: https://github.com/udayshankark/PAA11_1/blob/master/prompt_II.ipynb

# Visualization images and report(used_car_sales.pdf) are located in the /images folder : https://github.com/udayshankark/PAA11_1/tree/master/images
