# **Cropify: Automated Irrigation System**

## **Introduction**
Efficient irrigation is a critical factor in modern agriculture. This project, **Cropify**, addresses the challenge by implementing an **Automated Crop Management System** using the **A\*** search algorithm to optimize irrigation routes. By dynamically managing irrigation based on soil moisture levels and crop water needs, the system enhances resource efficiency and improves overall crop yield.

---

## **Objectives**
1. Develop an **A\*** search-based algorithm to determine optimal irrigation paths.
2. Integrate constraints such as limited water resources and crop-specific water needs.
3. Simulate the system on a grid farm representing soil moisture and crop water requirements.
4. Visualize the irrigation path on a grid for better interpretability.

---

## **System Overview**

### **Inputs**
1. **Grid Dimensions:** Represents the farm layout (rows × columns).
2. **Soil Moisture Levels:** Random values between 1 and 10 for each cell.
3. **Crop Water Needs:** Random values between 5 and 15 for each cell.
4. **Water Limit:** The total water available for irrigation (e.g., 150 units).

### **Outputs**
1. **Updated Soil Moisture Levels:** Reflects the grid after irrigation.
2. **Total Water Used:** The amount of water consumed during irrigation.
3. **Irrigation Path:** Sequence of cells visited for irrigation.
4. **Graph Visualization:** Displays the grid and the irrigation path.

---

## **Algorithm**
The **A\*** search algorithm is used to determine the most efficient irrigation path. The algorithm minimizes the cost of moving across the grid while ensuring irrigation constraints are satisfied.

### **Key Components**
1. **Cost Function:** Combines movement cost and a heuristic (distance to the farthest cell).
2. **Irrigation Logic:** Determines the amount of water needed for each cell, constrained by available water.
3. **Path Tracking:** Keeps track of all visited cells in the optimal irrigation path.

### **Algorithm Steps**
1. Initialize the grid with random soil moisture levels and crop needs.
2. Use the **A\*** search algorithm to navigate the grid:
   - Start from the top-left corner of the grid.
   - Visit neighboring cells with the least cost.
   - Update the soil moisture of each cell based on the water needs and available water.
3. Stop when water resources are exhausted or all cells are irrigated.

---

## **Visualization**
The system includes a graph visualization using **Matplotlib**:
1. The farm grid is represented as a heatmap, where the color intensity indicates soil moisture levels.
2. The irrigation path is shown as a red line connecting visited cells.
3. Grid lines and axis labels provide clarity, while a color bar indicates the moisture levels after irrigation.

---

## **Conclusion**
The **Cropify** system successfully optimizes irrigation for a simulated farm grid using the **A\*** search algorithm. By dynamically adjusting irrigation based on soil moisture and crop needs, the system demonstrates practical applications of AI in precision agriculture. The inclusion of visualization enhances interpretability, making it a valuable tool for resource-efficient farming.
