[Uploading datalab-output-Report_Portfolio1.pdf.md…]()


# Portfolio 1 Report: Procedural Store Shelf Generator

Rakhat Bektas

**Abstract - This is an innovative tool for the use in animation, 3D modeling and game development, which uses Blender's Geometry Nodes to create a Procedural Store Shelf Generator. This model allows users to create a variety of store environments by specifying the number of shelves and the types of items, greatly reducing the time needed to manually model.**

## I. INTRODUCTION

Procedural Store Shelf Generator is a model constructed using Blender modeling software. The model generates different store shelves depending on the number of the shelves and the collection of items(different shelves assets). This model might be useful in game development, animation, 3d scene creation. The main goal of this model is to generate store environment by adding procedurally generated store shelves which saves time when compared to creating each individually.

## II. IMPLEMENTATION

The main software used to create the model was Blender. Blender provides users with many tools in modelling, animation, texturing and others. But for this project focus was on Geometry Nodes functionality which is a procedural workflow, which – in simple terms – guides the software step by step through the completion of a set of operations based on user-defined parameters. The model mainly created using geometry nodes functionality which allowed the implementation of procedural creation of models.

The shelf structure starts with a new Group Input node that sets the initial geometry. Then the Subdivide Mesh node is used to increase the resolution of the mesh, a geometry of which. Flexibility is key with subdivision, so subdivide your shelf layout to create very detailed shelf designs that can be refined to fit a certain item size and shape.

The geometry can be manipulated further using Edge Neighbors and Dual Mesh nodes. Using the Edge Neighbors node, boundary information is extracted from each face in order to establish a framework for the shelf structure. The Dual Mesh node simply swaps the roles of faces and vertices;

converting the mesh into its dual form. This transformation simplifies shelf layout management, but does not sacrificed the flexibility of spawning many different configurations on the scene's need.

The second step is to convert the geometry into the curve, i.e using the Curve to Mesh node. But curves reduce the complexity of the operations and give a better control of the geometry. Then by applying the Resample Curve node to make sure that the points on the curve are uniformly distributed. useful when generating multiple shelves in a single model, in uniform distribution.

A series of Vector Math nodes such as Multiply and Add place and transform items on the shelves. Each instance of the shelf is also managed by these nodes, which control the position, rotation, and scale of the shelf. This allows for a very customizable placement of assets. The resampled curve is then converted to points, instances of shelves and items are placed dynamically in the Curve to Points node. That means that the shelves and its contents are kept evenly distributed and correctly laid into the model.

Realize Instances node handles the final step of procedural modeling process. This node, ensures that all the transformations done on the instances on the shelf (like scaling and placing) is done in the final geometry. If not for this step, the instances would remain abstract, so their transformations would not be applied on the output. Instances are realized, which means the generated shelves are able to be fully functioning and used in any application.

Once the model is completed, it gets output from the Group Output node, and the procedural workflow is ended. These nodes combined allow store shelves to be rapid generated with customized designs. The user is then able to create many different configurations of the shelf through varying input parameters, like shelf count and types of items. The final result of the structure is demonstrated on Figure 1.

![A complex Blender Geometry Node structure diagram showing a hierarchical flow of nodes for procedural shelf generation.](68ac34ff111db52afaa786afcb8346c3_img.jpg)

A complex Blender Geometry Node structure diagram showing a hierarchical flow of nodes for procedural shelf generation.

Fig. 1. Geometry Node structure

The assets used in this model were created using basic modeling techniques in Blender. The assets are displayed in figure 2.

![A row of six 3D assets: three teal bottles, a pink rectangular block, a blue sphere, a yellow rectangular block, and a grey rectangular block.](317e0525ef1b2458976c246876f4a948_img.jpg)

A row of six 3D assets: three teal bottles, a pink rectangular block, a blue sphere, a yellow rectangular block, and a grey rectangular block.

Fig. 2. Assets used

## III. RESULTS

The collection of assets used is increased and number of rows is customized. The results are not what was expected. The generation is not fully controlled and the model has some kind of pattern that takes over. The algorithm is not fully complete which why it gives this result with a pattern. The pattern changes if the number of rows:  $X*2$ ;  $X*3$ ;  $X*4$ ;  $X*5$ ;  $X*6$ . There are 5 different patterns that the model can produce at the moment meaning there is still room for improvement. Two types of patterns are displayed on figures 4 and 4.

![A 10x10 grid of 100 small 3D shelf units, each containing a different colored asset (bottles, blocks, sphere) in a repeating pattern.](8c378a184b5ae4d1605cb74d7b7a7e3f_img.jpg)

A 10x10 grid of 100 small 3D shelf units, each containing a different colored asset (bottles, blocks, sphere) in a repeating pattern.

Fig. 3. Row number equal to 17

![A 10x18 grid of 180 small 3D shelf units, showing a more complex and varied pattern of assets compared to Figure 3.](f5f48eb1753d75fb380cf01027a6395d_img.jpg)

A 10x18 grid of 180 small 3D shelf units, showing a more complex and varied pattern of assets compared to Figure 3.

Fig. 4. Row number equal to 18

## IV. DISCUSSION

This Procedural Store Shelf Generator has a lot of advantages in fields such as animation, 3D modeling and game development. It enables fast creation of realistic store environments in animation, reducing time spent manually modeling shelves while maintaining the ability to change shelf layout and item placement. It is ideal for building immersive scenes quickly.

The generator is used as a reusable asset for 3D modeling, which can be easily modified for different projects. The model can be used in various applications, such as architectural visualizations or interior designs, and the parameters, such as shelf size, spacing, and item configurations can be adjusted by designers.

The tool is especially useful for creating dynamic store environments in game development. Games often use procedural generation to populate large environments with repetitive elements such as shelves, to maintain consistency while saving on development time. It also allows for better performance by optimizing memory and reducing loading time by generating shelves on the fly.

The model, however, is currently limited to simple shelves, which restricts its use to more complex structures. Additional improvements could include more complex shelf types, random item placement, or dynamic damage for realism, expanding its applicability in a wider range of situations.

## V. CONCLUSION

Built with Blender's Geometry Nodes, the Procedural Store Shelf Generator is a fast and flexible way to build customizable store shelves for any field, including animation, 3D modeling, and game development. The procedural approach enables users to quickly and easily generate a variety of shelf configurations, reducing time and effort over manual modeling. The current model is optimized for simpler shelf designs but the complexity and realism could be improved in the future. In general, this tool demonstrates the benefits of procedural generation in speeding up development while keeping the freedom to use for different applications and environments.
