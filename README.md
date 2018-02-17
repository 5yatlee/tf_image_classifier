# CNN image classifier in tf 

## Dependency
* Tenforflow
* python


## Instruction

1. Retrain Mobilenet 

python -m scripts.retrain \
  --bottleneck_dir=tf_files/bottlenecks \
  --how_many_training_steps=1000 \
  --model_dir=tf_files/models/"mobilenet_0.50_224" \
  --summaries_dir=tf_files/training_summaries/"mobilenet_0.50_224" \
  --output_graph=tf_files/retrained_graph.pb \
  --output_labels=tf_files/retrained_labels.txt \
  --architecture="mobilenet_0.50_224" \
  --image_dir=tf_files/HEY



2. Test it

python -m scripts.label_image \
    --graph=tf_files/retrained_graph.pb  \
    --image=tf_files/unlabel/SAMPLE.jpg



Source:
https://codelabs.developers.google.com/codelabs/tensorflow-for-poets/index.html