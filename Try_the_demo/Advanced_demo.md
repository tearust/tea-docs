Assuming you have done the [Easy Start Demo](./Easy_start.md) first. If not, please try that first. Many concepts and workflows are the same as Easy Start, and we will ignore them.

# Deploy or ad-hoc?

In the Easy Start, we did not deploy our code and data. We just run the existing code and data. The code is a Tensorflow Image Recognization function; the data is a picture of a lion. We run a test and get the result.

Now let's move one step further learning ad-hoc.

When you want to use an existing Tensorflow Image Recognization function to detect your picture, the function code has been deployed by other developers. You need to upload your image. In this case, the code is deployed, your image (data) is ad-hoc. 

On the other hand, if someone deployed an image, but you developed a newer version of an image recognization algorithm code. You want to run your code against the existing image to verify your algorithm. In this case, the image is deployed, but your code is ad-hoc.

# Run demo for each scenario.
Please follow the sequence, try the first demo first. The second demo's instruction is much simpler since many steps are the same as the first one.

## Deploy data first, then run the code ad-hoc
Follow the instruction [here](./Deploy_data_run_adhoc_code.md)

## Deploy code first, then run the data ad-hoc
Follow the instruction [here](./Deploy_code_run_adhoc_data.md)


