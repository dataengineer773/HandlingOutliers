We have outliers in your data that you want to identify, and then reduce their impact on the data
distribution, Typically we have three strategies we can use to handle outliers. First, we can drop them, Second, we can mark them as outliers and include it as a feature, Finally, we can transform the feature to dampen the effect of the outlier
Similar to detecting outliers, there is no hard-and-fast rule for handling them. How we handle them
should be based on two aspects. First, we should consider what makes them an outlier. If we believe
they are errors in the data such as from a broken sensor or a miscoded value, then we might drop the
observation or replace outlier values with NaN since we can’t believe those values. However, if we
believe the outliers are genuine extreme values (e.g., a house [mansion] with 200 bathrooms), then
marking them as outliers or transforming their values is more appropriate.
Second, how we handle outliers should be based on our goal for machine learning. For example, if we
want to predict house prices based on features of the house, we might reasonably assume the price for
mansions with over 100 bathrooms is driven by a different dynamic than regular family homes.
Furthermore, if we are training a model to use as part of an online home loan web application, we might
assume that our potential users will not include billionaires looking to buy a mansion.
So what should we do if we have outliers? Think about why they are outliers, have an end goal in mind
for the data, and, most importantly, remember that not making a decision to address outliers is itself a
decision with implications.
One additional point: if you do have outliers standardization might not be appropriate because the mean
and variance might be highly influenced by the outliers. In this case, use a rescaling method more robust
against outliers like RobustScaler.
