A simple Co-op Carpentry Game where players can take orders, build, paint and sell them.

Players can interact with items and stations by interact key which is set to "E" by default. For the sake of simplicity, all the machine and platforms are grouped as stations.

Workbench can be used to take an order. Orders are generated at random times varying between 10 and 30 seconds. This can be changed in BP_GameState blueprint by changing min and max random time variables. Maximum amount of orders can be changed using MaxOrderAmount variable.

Furnitures can be spawned by interacting with chipping machine. Furnitures are defined in BPDA_FurnitureList blueprint. To add new furniture, a new item to the FurnitureItems array should be added with proper attributes are set. If the item is paintable, meshes material must have a linear color parameter called ColorCustom that corresponds to the part that is paintable.

Colors are predefined in E_ItemColors. After adding color to the enum, ItemColors variable in GameState should be added the linear color matching the newly added enum.

Players can place the furniture on top of Painting Machine and interact with paint boxes to paint it. Paint boxes can be modified simply by adding BP_PaintBox in BP_PaintMachine and selecting its color. Additionally painting has a cost which can be set in Game State blueprint.

After the modification of furnitures are done, players should bring them to Order Platform. If color of the item doesn't match with the order, players earn half of its price. If item type doesn't match then nothing happens except losing the furniture.

The game is modified to be played with 4 players but if it increases, after placing new Player Start to the level, NumberOfPlayers variable in BP_GameMode should be changed. 
