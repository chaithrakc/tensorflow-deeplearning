# Introduction to Tensorflow

```jsx
model = keras.Sequential([keras.layers.Dense(units=1, input_shpae=[1])])
```

The simplest possible neural network is one that has only one neuron in it, and that's what the above line of code does.

The above code is written using an API in TensorFlow library called keras.
In keras, "dense" define a layer of neurons fully connected to its adjacent layers. There is only one dense layer here and there is only one unit in it, so its a single neuron.
Successive layers are defined in sequence, hence the word "sequential."
Define the shape of what's input to the neural network in the first and in this case the only layer, and you can see that our input shape is super simple. It's just one value.

There are two function roles that you should be aware of though and these are loss functions and optimizers. The below code defines them.

```jsx
model.compile(optimizer='sgd', loss='mean_squared_error')
```

The neural network has no idea of the relationship between X and Y, so it makes a guess. Say it guesses Y= 10X - 10. It will then use the data that it knows about, that's the set of Xs and Ys that we have already seen to measure how good or how bad its guess was. The loss function measures this and then gives the data to the optimizer which figures out the next guess. So the optimizer thinks about how good or how badly the guess was done using the data from the loss function. And the logic is that each guess should be better than the one before. As the guesses get better and better, an accuracy approaches 100 percent, the term convergence is used.

```jsx
xs = np.array()
ys = np.array()
```

```jsx
model.fit(xs, ys, epochs=500) # training takes place here
```

```jsx
print(model.predict([10.0]))
```

when the model has finished training, it will give you back values using predict method.

Reasons for inaccurate prediction with [10.0]

1. trained using very little data. There are only 6 points
2. The 6 input points are linear but there is no guarantee that for every X, the relationship will be Y=2X-1. There is a very high probability that Y=19 for X=10, but the neural network is not positive. So it will figure out a realistic value for Y. When using neural networks, as they try to figure out the answers for everything, they deal in probability.