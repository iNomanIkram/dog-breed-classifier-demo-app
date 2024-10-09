# Dog Breed Classifier - CoreML Model

This CoreML model is trained to classify **60+ dog breeds** using a dataset containing **over 1.8 million images**. With this model, you can easily identify the breed of a dog from an image input.

## Supported Breeds
The model is capable of identifying the following dog breeds:

• Affenpinscher • African • Airedale • Appenzeller • Basenji • Beagle • Bluetick • Borzoi • Bouvier • Boxer • Brabancon • Briard • Bulldog • Bullterrier • Cairn • Cattle Dog • Chihuahua • Chow • Clumber • Cockapoo • Collie • Coonhound • Corgi • Cotondetulear • Dachshund • Dalmatian • Dane • Deerhound • Dhole • Dingo • Doberman • Elkhound • Entlebucher • Eskimo • Frise • German Shepherd • Greyhound • Groenendael • Hound • Husky • Keeshond • Kelpie • Komondor • Kuvasz • Labrador • Leonberg • Lhasa • Malamute • Malinois • Maltese • Mastiff • Mexican Hairless • Mix • Mountain • Newfoundland • Otterhound • Papillon • Pekingese • Pembroke • Pinscher • Pointer • Pomeranian • Poodle • Pug • Puggle • Pyrenees • Redbone • Retriever • Ridgeback • Rottweiler • Saluki • Samoyed • Schipperke • Schnauzer • Setter • Sheepdog • Shiba • Shih Tzu • Spaniel • Springer • St. Bernard • Terrier • Vizsla • Weimaraner • Whippet • Wolfhound

## Test the Model

You can test the model using our **iOS Demo Application**.

![Demo Application Screenshot](https://github.com/iNomanIkram/dog-breed-classifier-demo-mobile-ios-app/blob/main/demo-app.png)

### Quick Start Instructions

1. Copy **ImageProcessor.swift** to the root folder of your project.
2. Initialize the model in your code:
   ```swift
   let model = Dog_Breeds_Classifier()
   ```
3. Use the following method to process an image and return the breed name:
   ```swift
   // Process the image to identify the dog's breed
   func breedLabel(forImage image: UIImage) -> String? {
       if let imageBuffer = ImageProcessor.pixelBuffer(forImage: image.cgImage!) {
           guard let breed = try? model.prediction(image: imageBuffer) else { fatalError("Prediction error") }
           return breed.classLabel
       }
       return nil
   }
   ```

For further instructions and code examples, feel free to explore the demo app repository!

---
