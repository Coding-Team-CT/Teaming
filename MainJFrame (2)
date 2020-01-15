\\\/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package JmainFrame;

import java.awt.BorderLayout;
import java.awt.Container;
import java.awt.GridLayout;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;
import java.io.File;
import java.io.FileInputStream;
import java.util.ArrayList;
import java.util.Iterator;
import java.util.LinkedList;
import java.util.List;
import java.util.Queue;
import java.util.TreeMap;
import java.util.TreeSet;


import javax.swing.JButton;
import javax.swing.JFileChooser;
import javax.swing.JFrame;
import javax.swing.JPanel;
import javax.swing.JTextField;
import javax.swing.text.SimpleAttributeSet;
import javax.swing.text.StyleConstants;
import javax.swing.text.StyledDocument;
import org.apache.poi.ss.usermodel.Cell;
import org.apache.poi.ss.util.CellRangeAddress;

import org.apache.poi.ss.usermodel.Row;
import org.apache.poi.ss.format.CellFormatType;
import org.apache.poi.ss.usermodel.*;
import org.apache.poi.xssf.usermodel.XSSFCellStyle;
import org.apache.poi.xssf.usermodel.XSSFFont;
import org.apache.poi.xssf.usermodel.XSSFSheet;
import org.apache.poi.xssf.usermodel.XSSFWorkbook;
import org.apache.poi.openxml4j.exceptions.InvalidFormatException;

/**
 * 
 *
 * @author ENG_Ahmed
 */
public class MainJFrame extends javax.swing.JFrame {
     int noOfNo=0;
       public Queue HeadersQueue = new LinkedList();
       public Queue leftAtrrib = new LinkedList();

      boolean TblName=false;
      int intTableNo;
      public Queue queueA = new LinkedList();
    
    int RowsNo;
    int ColumsNo;
    int RealRowsNo;
    int RealColumsNo;
    boolean BlnReverse;
    boolean IsFrsCel;
    //int noOfData;
   
    int CellsNo;
    int CellPerRow;
     String temp;
    String[][] multiRows;
    public Queue HeadersQueue2 = new LinkedList();
   boolean [][]AttPos;
    double[][] multiRows2;
    boolean SecondTable ;
    int RealRowsNo2;
    int RealColumsNo2;
    boolean BlnReverse2;
    int noOfData2;
    String Cell_val;
    public int noOfNo2;
    int CellsNo2;
    boolean FirstRow = false;
      String TablName=""; 
       boolean TorF;
       boolean blank=false;
       boolean TablNm = false;
       short lastCellNum ;
       int phNumOfCell;
       boolean firstRow = false;
         String StrAdress;
         int frColAdress;
         int lstColAdress;
        int NmRwAdress;
        int NmOfCells;
         boolean RealfirstRow;
          int firstRowNm;
          boolean FrstDummy = false;
          int nmOfMg=0;
                int lstRowNm=0; 
                    boolean leftAtt  = false;
                    int leftParentRow=0;
                    boolean check = false;
                     String strValue= " ";
                     int nmOfCell = 0;
                     int firstRownm=0;
                        boolean secondLeftAtt = false;
                        boolean rightAtt=false;
                      //  boolean leftAtt = false;
          
     public  class Node<T>{
    private T data;
    private int index ;
    private char c ;
    private Node<T> parent ,Neighbour;
    private List<Node<T>> childern;
               Node (){
                    }
     Node (T rootData){
        
        this.data = rootData;
       this.childern = new ArrayList<Node<T>>();
    }
    
    public Node<T> addChild(T data , int indx ,char ch){
    Node<T> childNode = new Node<T>(data);
    //this.c = ch;
    childNode.parent = this;
    this.childern.add(childNode);
        childNode.index = indx;
        childNode.c = ch;
    return childNode;

    }
     public Node<T> getChild( int n ){
          
             Node<T> childNode = new Node<T>(data);

            if (n < childern.size()){
                 childNode = childern.get(n);
             return childNode;
                }
             return null;
                 }
      public void setNeighbour(Node<T> neighbour){
                  this.Neighbour = neighbour;
              }
      public boolean remove(int Index){
          if (this.getChild(Index) != null){
          this.childern.remove(this.getChild(Index));
         
          return true;
          }
          else 
              return false;
          
      }
       public boolean RemoveAll(){
           
             if (!childern.isEmpty()){
             this.childern.removeAll(childern);
              return true;}
              else return false;
         }

     }
     
                   Node<String> parent,RightParent,LeftParent,currentParent,currentLeftParent,currentRightParent; 
            
                       Node<String> tempNode,prvNode,topParent ; 
                       Node<String> firstNextRowChild,root,DummyParent,Dummy,currentDummyParent;                
               
                //



       //int lastRow;

    /**
     * Creates new form MainJFrame
     */
    public MainJFrame() {
        this.AttPos = new boolean[][]{{false}, {false}};
        this.Cell_val = " ";
        initComponents();
    }

    /**
     * This method is called from within the constructor to initialize the form.
     * WARNING: Do NOT modify this code. The content of this method is always
     * regenerated by the Form Editor.
     */
    @SuppressWarnings("unchecked")
    // <editor-fold defaultstate="collapsed" desc="Generated Code">//GEN-BEGIN:initComponents
    private void initComponents() {

        jButton1 = new javax.swing.JButton();
        jButton2 = new javax.swing.JButton();
        jScrollPane1 = new javax.swing.JScrollPane();
        jTextPane1 = new javax.swing.JTextPane();

        setDefaultCloseOperation(javax.swing.WindowConstants.EXIT_ON_CLOSE);

        jButton1.setText("Open");
        jButton1.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                jButton1ActionPerformed(evt);
            }
        });

        jButton2.setText("Clear ");
        jButton2.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                jButton2ActionPerformed(evt);
            }
        });

        jScrollPane1.setViewportView(jTextPane1);

        javax.swing.GroupLayout layout = new javax.swing.GroupLayout(getContentPane());
        getContentPane().setLayout(layout);
        layout.setHorizontalGroup(
            layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(layout.createSequentialGroup()
                .addGap(275, 275, 275)
                .addComponent(jButton1)
                .addGap(42, 42, 42)
                .addComponent(jButton2)
                .addContainerGap(292, Short.MAX_VALUE))
            .addGroup(javax.swing.GroupLayout.Alignment.TRAILING, layout.createSequentialGroup()
                .addComponent(jScrollPane1)
                .addContainerGap())
        );
        layout.setVerticalGroup(
            layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(javax.swing.GroupLayout.Alignment.TRAILING, layout.createSequentialGroup()
                .addContainerGap()
                .addComponent(jScrollPane1, javax.swing.GroupLayout.PREFERRED_SIZE, 273, javax.swing.GroupLayout.PREFERRED_SIZE)
                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    .addComponent(jButton1)
                    .addComponent(jButton2))
                .addContainerGap(22, Short.MAX_VALUE))
        );

        pack();
    }// </editor-fold>//GEN-END:initComponents

    private void jButton1ActionPerformed(java.awt.event.ActionEvent evt) {//GEN-FIRST:event_jButton1ActionPerformed
        // TODO add your handling code here:
        FileChooserClass ff = new FileChooserClass();
        String Filepath = ff.getFilePath();
        //ReadExcel RR = new ReadExcel(FilePath);
        ReadExcel(Filepath);
    }//GEN-LAST:event_jButton1ActionPerformed

    private void jButton2ActionPerformed(java.awt.event.ActionEvent evt) {//GEN-FIRST:event_jButton2ActionPerformed
        // TODO add your handling code here:
        jTextPane1.setText("");
    }//GEN-LAST:event_jButton2ActionPerformed
   public void displayTopAtt(){
         StyledDocument doc = jTextPane1.getStyledDocument();
        SimpleAttributeSet keyWord = new SimpleAttributeSet();
        StyleConstants.setBold(keyWord, true);
        String element ="";
          String nelement ="";

        try {
            if (rightAtt ){
              doc.insertString(doc.getLength(), "\n" +  " top Attributes : \n", keyWord );

             Node <String> topAtt,nextAtt;
    nextAtt = null;
    topAtt = DummyParent.Neighbour;
    if (Dummy != null)
     nextAtt = DummyParent.getChild(0).Neighbour;
    System.out.println("else statement :");
    
    do{ 
    while (topAtt != null && topAtt.Neighbour != null){
     System.out.println("\ntopAtth:"+topAtt.data);
     element = topAtt.data;
      if (nelement != element)
         doc.insertString(doc.getLength(),  element  +  " \t", keyWord );

     if (  topAtt.Neighbour != null)
      topAtt = topAtt.Neighbour;
      System.out.println("\ntopAtt nighbour:"+topAtt.data);
           nelement = topAtt.data;
               
                    
              doc.insertString(doc.getLength(),  nelement  +  " \t", keyWord );
               
    }
    if (nextAtt != null  ){
    topAtt = nextAtt;
    System.out.println("topAtt"+topAtt.data);
    nextAtt = nextAtt.getChild(0);
      System.out.println("nextAtt"+nextAtt.data);
    doc.insertString(doc.getLength(), "\n" , keyWord );
    }

    }while ( nextAtt != null && nextAtt.data != DummyParent.data && topAtt.c != 'v' );
            
                    
  
    }
            
        
        } catch(Exception e) { System.out.println(e);}
        
}
    public void displayValue(){
         StyledDocument doc = jTextPane1.getStyledDocument();
        SimpleAttributeSet keyWord = new SimpleAttributeSet();
        StyleConstants.setBold(keyWord, true);
        String element ="";
    try{
        if (LeftParent.getChild(0)!= null)
       doc.insertString(doc.getLength(), "\n" + "Vlaues: \n", keyWord );
       if (leftAtt){
           
      int i =0;
    int k =0;
    int y=0;
    int j =0;
    boolean cKey =false;
     boolean vKey =false;
     
    Node  <String>lParent,vParent,cParent,hParent;
           System.out.println("rlparent :"+LeftParent.data);

   while (LeftParent.getChild(y)!= null && LeftParent.getChild(y).data != LeftParent.data ){
       k =0;
    lParent = LeftParent.getChild(y);
       System.out.println("rlparent :"+lParent.data);
      // if (k ==0)
       while (lParent.getChild(k)!= null && lParent.getChild(k).data != lParent.data ){
           i =0;
           cParent = lParent.getChild(k);
                  System.out.println("cparent :"+cParent.data +" data type :"+cParent.c);
                  if( cParent.c == 'v' &&  cParent.index == lParent.index){
                      element = lParent.getChild(k).data;
                     doc.insertString(doc.getLength(),  element+"\t", keyWord );  
                  
                  }
                    else{
                        cKey = true;
                       }
                 
                  while(cParent.getChild(i)!= null && cParent.getChild(i).data != cParent.data){
                      j =0;
                  vParent = cParent.getChild(i);
                        System.out.println("vParent :"+vParent.data);
                       if( vParent.c == 'v' && vParent.index == cParent.index){
                      element = cParent.getChild(i).data;
                     doc.insertString(doc.getLength(),  element+"\t", keyWord );  
                  
                  }
                       else{
                       vKey = true;
                       }
                        while (vParent.getChild(j)!= null && vParent.getChild(j).data != vParent.data){
                        hParent = vParent.getChild(j);
                         System.out.println("hparent :"+hParent.data);
                         if( hParent.c == 'v' && hParent.index == vParent.index){
                      element = vParent.getChild(i).data;
                     doc.insertString(doc.getLength(),  element+"\t", keyWord );  
                  
                  }
                       
                         j++;
                        }
                        if (vKey == true)
                         doc.insertString(doc.getLength(),  "\n", keyWord );
                    i++;
                  }
                    if (cKey == true)
                        doc.insertString(doc.getLength(),  "\n", keyWord );

                 k++;
               }
               //   if (y ==0)
           doc.insertString(doc.getLength(),  "\n", keyWord );
                 

         y++;
    
    }
       }
       
       
       
    }catch(Exception e) { System.out.println(e); }
    }
    public void displayLeftAtt(){
        StyledDocument doc = jTextPane1.getStyledDocument();
        SimpleAttributeSet keyWord = new SimpleAttributeSet();
        StyleConstants.setBold(keyWord, true);
        String element ="";
          int i =0;
    int k =0;
    int y=0;
    int j =0;
    Node  <String>lParent,vParent,cParent,hParent;
        try{
            if (leftAtt){
                doc.insertString(doc.getLength(),  "\n"+"Left Attribut:\n", keyWord ); 

           System.out.println("rlparent :"+LeftParent.data);

   while (LeftParent.getChild(y)!= null && LeftParent.getChild(y).data != LeftParent.data ){
       k =0;
    lParent = LeftParent.getChild(y);
       System.out.println("rlparent :"+lParent.data);
                      element = lParent.data;
                     doc.insertString(doc.getLength(),  "\n  "+element, keyWord ); 
       while (lParent.getChild(k)!= null && lParent.getChild(k).data != lParent.data ){
           i =0;
           cParent = lParent.getChild(k);
                  System.out.println("cparent :"+cParent.data);
                    if( cParent.c == 'l' ){
                      element = lParent.getChild(k).data;
                     doc.insertString(doc.getLength(), "\n "+ element, keyWord );  
                    }
                  while(cParent.getChild(i)!= null && cParent.getChild(i).data != cParent.data){
                      j =0;
                     vParent = cParent.getChild(i);
                        System.out.println("vparent :"+vParent.data);
                        if( vParent.c == 'l' ){
                      element = cParent.getChild(i).data;
                     doc.insertString(doc.getLength(), "\n"+ element, keyWord );  
                    }
                        while (vParent.getChild(j)!= null && vParent.getChild(j).data != vParent.data){
                        hParent = vParent.getChild(j);
                         System.out.println("hparent :"+hParent.data);
                         j++;
                        }
                    i++;
                  }
                 k++;
               }
         y++;
    
    }
    
            }
        }catch(Exception e) { System.out.println(e); }
    
    }
    public void displayValue2(){
     StyledDocument doc = jTextPane1.getStyledDocument();
        SimpleAttributeSet keyWord = new SimpleAttributeSet();
        StyleConstants.setBold(keyWord, true);
        String element ="";
        try{
              Node <String> topAtt;
            if (rightAtt && !leftAtt){
               doc.insertString(doc.getLength(), "\n " +  " value: \n", keyWord );  
      
      int i =0;
    if (rightAtt ){
    topAtt = DummyParent.Neighbour;
   if (Dummy != null)
     topAtt = Dummy.Neighbour;
    do {
    while (topAtt != null  && topAtt.getChild(i)!= null){
    System.out.println("\ntopAtth:"+topAtt.data);
        System.out.println("\ntopAtt Value: "+topAtt.getChild(i).data);
              element = topAtt.getChild(i).data;
                  doc.insertString(doc.getLength(),  element +" \t", keyWord );  

   
       topAtt = topAtt.Neighbour;
   
    }
        doc.insertString(doc.getLength()," \n", keyWord );  

    
   if (Dummy != null)
     topAtt = Dummy.Neighbour;
   else 
        topAtt = DummyParent.Neighbour;
    
    
    i ++;
    }while ( topAtt.getChild(i) != null && topAtt.c != 'v' );
     }
    
        System.out.println("remove ==================");
    topAtt = DummyParent;
   if (Dummy != null)
     topAtt = Dummy;
    System.out.println("top "+ topAtt.data);
    while (topAtt != null  && topAtt.getChild(0)!= null){
             System.out.println("\ntopAtth:"+topAtt.data);
              topAtt.remove(0);
              if (topAtt.getChild(0) != null)
             System.out.println("\ntopAtt Value: "+topAtt.getChild(0).data);
   
             topAtt = topAtt.Neighbour;
        }
            }
        
        
        }catch(Exception e) { System.out.println(e); }
    }
    public void displayBoldText () {
        StyledDocument doc = jTextPane1.getStyledDocument();
        SimpleAttributeSet keyWord = new SimpleAttributeSet();
        StyleConstants.setBold(keyWord, true);
        String element ="";
        String pos="";
        int count=0;
        int i;
        int j =0;
       // int  cunOf[]={3,2,1,1,1,1,1,1,1,1,4};

        try
        {
            //if (HeadersQueue.size() >0){
            if (TblName == false)
                intTableNo ++;
                doc.insertString(doc.getLength(), "\n " +  " Attributes : \t", keyWord );  
                doc.insertString(doc.getLength(), "\n", keyWord );

                      int x =doc.getLength();

            //}
            //access via Iterator
            Iterator iterator = HeadersQueue.iterator();
            while(iterator.hasNext()){

                element = iterator.next().toString();
                 //pos =  iterator.next().toString();
                if(element == "End"){
                        if(count == 0){
                        count++;
                        }
                        else{
                            if(count == 1){
                           count++;

                       doc.insertString(doc.getLength(), "\n " +  " top Attributes : \t", keyWord );  
                       doc.insertString(doc.getLength(), "\n", keyWord );
                            }
                         else
                       doc.insertString(doc.getLength(), "\n", keyWord );
                        }
                }
                else{
                    
                    if(element != "End"){
                       
                     //for (i=0;i<cunOf[j];i++){  
                         element = element + "\t";
                          doc.insertString(doc.getLength(), element, keyWord );

                
               System.out.println("doc lenth:"+x+element+"element length;"+element.length());
                    }
                }
            }
            Iterator iteratora = leftAtrrib.iterator();
                    doc.insertString(doc.getLength(), "\n " +  " left Attributes : \n", keyWord );  

            while(iteratora.hasNext()){

                element = iteratora.next().toString();
            
            doc.insertString(doc.getLength(), element+"\n", keyWord );
            }
            //access via new for-loop
            iterator = HeadersQueue.iterator();
            while(iterator.hasNext()){
                Object firstElement = HeadersQueue.remove();
            }        
             iterator = leftAtrrib.iterator();
            while(iterator.hasNext()){
                Object RemovElement = leftAtrrib.remove();
            }        
            //doc.insertString(doc.getLength(), "\n", keyWord );
        }
        catch(Exception e) { System.out.println(e);}
    }
   
    public void displayPlainText () {
        StyledDocument doc = jTextPane1.getStyledDocument();
        SimpleAttributeSet keyWord = new SimpleAttributeSet();
        StyleConstants.setBold(keyWord, false);
        try
        {
            String element ="";
            doc.insertString(doc.getLength(), "\n Table "+ intTableNo + " Values : \n", keyWord );
            for (int i = 0; i<=RealColumsNo;i++)
            {
                for (int j = 0; j<RealRowsNo;j++)
                {
                    element = multiRows[j][i];
                    if (element ==null)
                        break;
                    element = element + "\t";
                    doc.insertString(doc.getLength(), element, keyWord );
                    multiRows[j][i] = null;
                }
                doc.insertString(doc.getLength(), "\n", keyWord );
            }
            
                
            //Arrays.fill(multiRows, null); 
            doc.insertString(doc.getLength(), "\n", keyWord );
            RealRowsNo =0;
            BlnReverse = false;
            RealColumsNo = 0;
        }
        catch(Exception e) { System.out.println(e); }
    }
    public void displayTableName2 (String TbName) {
        StyledDocument doc = jTextPane1.getStyledDocument();
        SimpleAttributeSet keyWord = new SimpleAttributeSet();
        StyleConstants.setBold(keyWord, true);
        String element ="";
        
        try
        {
            //if (HeadersQueue.size() >0){
           // intTableNo ++;
            doc.insertString(doc.getLength(), "\n " + "Table " + intTableNo + " Name : ", keyWord );    
            //}
            //access via Iterator
            //Iterator iterator = HeadersQueue2.iterator();
            //while(iterator.hasNext()){
              //  element = iterator.next().toString();
               // element = element + "\t";
               if (TablNm){
                doc.insertString(doc.getLength(),TbName, keyWord );
                
           // }
           // doc.insertString(doc.getLength(), "\n", keyWord );
            //access via new for-loop
           // iterator = HeadersQueue2.iterator();
           // while(iterator.hasNext()){
           //     Object firstElement = HeadersQueue2.remove();
            //}           
            //doc.insertString(doc.getLength(), "\n", keyWord );
            
               }
        }
        catch(Exception e) { System.out.println(e); }
    }
    
    /**
     * @param args the command line arguments
     */
    public static void main(String args[]) {
        /* Set the Nimbus look and feel */
        //<editor-fold defaultstate="collapsed" desc=" Look and feel setting code (optional) ">
        /* If Nimbus (introduced in Java SE 6) is not available, stay with the default look and feel.
         * For details see http://download.oracle.com/javase/tutorial/uiswing/lookandfeel/plaf.html 
         */
        try {
            for (javax.swing.UIManager.LookAndFeelInfo info : javax.swing.UIManager.getInstalledLookAndFeels()) {
                if ("Nimbus".equals(info.getName())) {
                    javax.swing.UIManager.setLookAndFeel(info.getClassName());
                    break;
                }
            }
        } catch (ClassNotFoundException ex) {
            java.util.logging.Logger.getLogger(MainJFrame.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (InstantiationException ex) {
            java.util.logging.Logger.getLogger(MainJFrame.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (IllegalAccessException ex) {
            java.util.logging.Logger.getLogger(MainJFrame.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (javax.swing.UnsupportedLookAndFeelException ex) {
            java.util.logging.Logger.getLogger(MainJFrame.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        }
        //</editor-fold>

        /* Create and display the form */
        java.awt.EventQueue.invokeLater(new Runnable() {
            public void run() {
                new MainJFrame().setVisible(true);
                
            }
        });
    }

    // Variables declaration - do not modify//GEN-BEGIN:variables
    private javax.swing.JButton jButton1;
    private javax.swing.JButton jButton2;
    private javax.swing.JScrollPane jScrollPane1;
    private javax.swing.JTextPane jTextPane1;
    // End of variables declaration//GEN-END:variables

     public void ReadExcel(String FilePath) 
	{
            try
		{
			//FileInputStream file = new FileInputStream(new File(FilePath));

			//Create Workbook instance holding reference to .xlsx file
			//XSSFWorkbook workbook = new XSSFWorkbook(file);
                        Workbook workbook2 = WorkbookFactory.create(new File(FilePath));

                       // HssfWorkbook hssWorkbook = new HssfWorkbook (file);
                         // for (int i = 0; i < workbook2.getNumberOfSheets(); i++) 
                          {
                                  Sheet sheet = workbook2.getSheetAt(0);

                            SecondTable = false;
                        do{
                                //HSSFSheet mySheet = myWorkBook.getSheetAt(i);  
                        // TablName="";
                        
                        firstRow = false;
                         intTableNo =1;
                          TablNm =false;
                             RowsNo = 0;                     
                             TablName = " Non";
                             leftAtt = false;
                             rightAtt = false;
                             RealfirstRow= false;

                           System.out.println("table name:"+TablNm);
                         System.out.println("sheet nm:"+0);
                         
                         int Pysrow = sheet.getPhysicalNumberOfRows();
                             System.out.println("top : "+Pysrow);

                           int nmOfMgReg = sheet.getNumMergedRegions();
                          int PysRow =  sheet.getPhysicalNumberOfRows();
                         System.out.println("PysRow: "+PysRow);
                          CellRangeAddress adress = new CellRangeAddress(0,8,0,8);
                             firstRownm =  sheet.getFirstRowNum();
                               System.out.println("first row:"+sheet.getFirstRowNum());
                             
                            if  ( nmOfMgReg > 0 && adress != null)
                               {
                                   //for (int h =nmOfMgReg- 1; h >=0 ; h-- )
                                   {
                               adress =  sheet.getMergedRegion(0);
                               StrAdress = adress.toString();
                               frColAdress = adress.getFirstColumn();
                               NmOfCells = adress.getNumberOfCells();
                               NmRwAdress = adress.getFirstRow();
                               lstColAdress = adress.getLastColumn();
                               lstRowNm = adress.getLastRow();
                              nmOfMg =0;
                              System.out.println("last row index:"+lstRowNm +"adress as Srting:"+adress.formatAsString());
                       System.out.println(" Nm regions="+ nmOfMgReg +" \tfirst col of merged:"+frColAdress +"lstColAdress:"+lstColAdress+" \tnumber of cells:"+NmOfCells+"\t row:"+NmRwAdress);
                                   }
                      // System.out.println("top row:"+sheet.getTopRow());
                              if (adress != null)

                               System.out.println("PhysicalNumberOfRows:"+ PysRow+"merged:"+ adress);
                               }
                            
      
                       int  lastRow = sheet.getLastRowNum();
                       int Columnbreak[] = new int [10];
                                  Columnbreak =   sheet.getColumnBreaks();
                                  for (int x = 0; x < Columnbreak.length; x++ ){
                         System.out.println("column break ("+x+")="+Columnbreak[x]);

                                  }
                        System.out.println("last row:"+sheet.getLastRowNum());
                                          
			Iterator<Row> rowIterator = sheet.iterator();
                        { 
                           
			while (rowIterator.hasNext()) 
			{
				Row row = rowIterator.next();
                                RowsNo++; 
                                 FirstRow = true;
                                  CellPerRow = 0;
                                  RealRowsNo =0;
                                      String prvCelValue = "non";
                                   System.out.println("tablname:"+TablNm);
                              System.out.println("Row Number : "+row.getRowNum());
                              System.out.println("first cell:"+row.getFirstCellNum());
                              Row rowv = sheet.getRow(RowsNo);
                              Row prvRow = sheet.getRow(RowsNo-1);
                              int RowNm = sheet.getPhysicalNumberOfRows();
                               if (row.getRowNum()<= sheet.getLastRowNum() && sheet.getRow(row.getRowNum()-1) == null && row.getRowNum()>5 ){
                                   
                                   
                         if (rightAtt )
                        displayTopAtt();
                 
                        displayLeftAtt();
                            displayValue2();
                            displayValue();
                           
                                   removeTopAtt();
                                   System.out.println("row num: " + "second table");
                              
                                firstRow = false;
                         intTableNo ++;
                          TablNm =false;
                             RowsNo = 0;                     
                             TablName = " Non";
                             leftAtt = false;
                             rightAtt = false;
                             RealfirstRow= false;
                                                      }
                             // System.out.println("column width: "+ sheet.getColumnWidth(i));
                           try {
                          //short bord = row.getRowStyle().getBorderBottom();
                         // System.out.println("borderbottom:"+bord);
                        System.out.println( "row border:"+ row.getRowStyle().getBorderBottom());
                           }  catch(Exception e) { System.out.println(e);}
                           
                              System.out.println("number of region = "+nmOfMg+"last row index:"+lstRowNm);
                       System.out.println(" Nm regions="+ nmOfMgReg +" \tfirst col of merged:"+frColAdress +"lstColAdress:"+lstColAdress+" \tnumber of cells:"+NmOfCells+"\t row:"+NmRwAdress);
                        
                               if(  rowv == null )
                               {
                               
                                   blank =true;
                            System.out.println("blank "+ blank );
                            

                               }
                              
                                System.out.println("rown="+RowsNo+" last row="+ lastRow);
                                 lastCellNum =   row.getLastCellNum();
                                  phNumOfCell   = row.getPhysicalNumberOfCells();
                                      int frstCelNm =  row.getFirstCellNum();
                                      nmOfCell =  lastCellNum - frstCelNm ;
                                  System.out.println("first cell number:"+frstCelNm+" last cell number :" +lastCellNum +" numbercell:"+nmOfCell+" physical number of cell:"+phNumOfCell );
                                 int k =0;
				//For each row, iterate through all the columns
				Iterator<Cell> cellIterator = row.cellIterator();
				
				while (cellIterator.hasNext()) 
				{
					Cell cell = cellIterator.next();
                                           
                                        
                                          
                       
                                        
                                        
                                        
                                         System.out.print(" is cell part :"+cell.isPartOfArrayFormulaGroup());
                                         cell.equals(rowv);
                                        Cell cel=  row.getCell(k);
                                        System.out.println(" cell (0):" + cel);
                                        if (row.getCell(k) != null  )
                                        System.out.println("formula:"+cel.getCellStyle());
                                          /*int lastColum = sheet.getColumnWidth(ColumsNo);
                                            System.out.println("columnWidth" +lastColum );*/
                                              k++;
                                          int c = cell.getColumnIndex();
					//Check the cell type and format accordingly
                                    System.out.println(" cell adress:" + c);
                                           

                                            
					switch (cell.getCellType()) 
					{
						case Cell.CELL_TYPE_NUMERIC:
                                                     blank= false;
                                                
                                                     if (FirstRow == true){
                                                         FirstRow =false;
                                                         /*if(firstNextRowChild != null)
                                                      currentRightParent = firstNextRowChild;*/
                                                         if (rightAtt && Dummy != null )
                                                         if (Dummy.Neighbour != null)
                                                             currentRightParent = Dummy.Neighbour;
                                                         System.out.println("leftAtt:"+leftAtt +" currentLeftParent:"+currentLeftParent.data);
                                                       /*  if (leftAtt && secondLeftAtt){
                                       
                                                        secondLeftAtt = false;
                                                        currentParent = LeftParent;
                                   
                                                       tempNode = currentParent.addChild(prvCelValue, cell.getRowIndex(),'l');
                                                       System.out.println("second left Attribute"+"\tparent :"+ currentParent.data + "\tdata:"+prvCelValue);

                                                        currentLeftParent = tempNode;
                                                           // currentParent = tempNode;
                                                             }*/
                                                 
                                                     }
                                                        double   CellValue = cell.getNumericCellValue();
                                              
                                              
                                                        if (currentLeftParent != null){
                                                       tempNode = currentLeftParent.addChild(Double.toString(CellValue), cell.getRowIndex(),'v');
                                                       System.out.println("value="+tempNode.data+"\tleft parent:"+currentLeftParent.data );
                                                        }
                                                        if (currentRightParent != null){
                                                       tempNode = currentRightParent.addChild(Double.toString(CellValue), cell.getColumnIndex(),'v');
                                                        
                                                      System.out.print( "value="+tempNode.data+"\t right parent :"+currentRightParent.data + "\tcurrentRightParent"+currentRightParent.data);
                                                        }
                                                        
                                                      if (currentRightParent != null && currentRightParent.Neighbour != null)    
                                                      currentRightParent = currentRightParent.Neighbour;
                                               
							break;
						case Cell.CELL_TYPE_STRING:
                         XSSFCellStyle style = (XSSFCellStyle)cell.getCellStyle();
                          CellStyle style2 = cell.getCellStyle();
                            String styleString = cell.getCellStyle().toString();
                            String style2String = cell.getCellStyle().toString();
                         //   style = (XSSFCellStyle)style2 ;
                             XSSFFont font = style.getFont();
                            Short font2 = style2.getFontIndex();
                            
                                 
                              int ee = font.getFontHeightInPoints();
                                 byte undrln = font.getUnderline();
                               //  font.getXSSFColor().getARGBHex();
                             //----------------------------
                            int yy2 =cell.getColumnIndex();
                             int xx2 = cell.getRowIndex();
                        //   String ccc = font.getXSSFColor().getARGBHex();
                           //String ccc = font.getXSSFColor().getARGBHex();
                             String CelColor="FF000001";
                             if (font.getXSSFColor() != null )
                             CelColor= font.getXSSFColor().getARGBHex();
                            boolean bb = font.getBold();
                            boolean dd =font.getItalic();
                           System.out.println("cell border:"+style.getBorderBottom());
                            //----------------------------
                            //  System.out.println("ccc="+ccc);
                             String CelValue = cell.getStringCellValue();
                         
                            boolean capitl = isAllCapital(CelValue);
                                
                            if( ee>11 || bb ||(!CelColor.equals("FF000000")) ||dd||capitl||undrln ==1 || Attribute(CelValue)){
                                
                            System.out.println("Attribute:"+" row-"+xx2+" co-"+" "+yy2+" "+CelValue);
                                                       CellPerRow ++;
                                                       System.out.println("attribute cell per row("+xx2+"):"+  CellPerRow );
                                                       System.out.println("TablNm:"+TablNm +" firstRownm: "+firstRownm+" xx2="+xx2 +"leftAtt: " +leftAtt);
                                if( !TablNm  &&!rightAtt && !leftAtt && (nmOfCell ==1 || CelValue.contains("able") || sheet.getRow(xx2+1) == null )  )
                                {
                                    
                                     Row blankRow = sheet.getRow(xx2+1);
                                     if (blankRow == null)
                                     System.out.println("null");
                                     
                                  
                                       
                                        blank = false;
                                        TablNm = true;
                                         System.out.println("tablname:"+TablNm);
                                       // else 
                                         Node<String > Table = new Node<String>("Table");
                                    TablName =CelValue;
                                    Table.data = TablName;
                                   displayTableName2(TablName);
                                   Table.data= CelValue;
                                   
                                    RightParent = Table.addChild("Right Attribute",0,'t');
                                  LeftParent = Table.addChild("Left Attribute",1,'l');
                                   currentParent=LeftParent;
                                  currentRightParent = RightParent;
                                  System.out.println("Table name:"+"row:"+xx2+"col:"+yy2+" "+Table.data);
                                  
                                }
                                else if ( phNumOfCell ==1 && yy2 == 0){
                                     leftAtt = true;
                                         
                                        if(xx2 == leftParentRow+1){
                                        
                                            leftParentRow = xx2;
                                            if (check ){
                                                    check = false;
                                             System.out.println("current parent before :"+LeftParent.data);
    
                                             tempNode = LeftParent.addChild(strValue, xx2,'l');
                                             currentParent = tempNode;
                                             
                                           
                                            }
                                             System.out.println("current parent before :"+currentParent.data);
                                            tempNode = currentParent.addChild(CelValue, xx2,'l');
                                         currentParent = tempNode;
                                         System.out.println("row number: "+xx2+"current parent :"+currentParent.data);
                                        }
                                        else{
                                             check = true;
                                            leftParentRow = xx2;
                                    strValue  = CelValue;
                                    System.out.println("xx2 :"+xx2 +"check"+check);

                                     System.out.println("row number: "+xx2+"left parent  Attribute"+CelValue+"\tat index:"+xx2 + "\tcurrent parent :"+currentParent.data);
                                    }
                                    
                                 
                                
                                }
                                else if (phNumOfCell > 1 && TablName == " Non" ){
                                    FirstRow = false;
                                     Node<String > Table = new Node<String>("Table");
                                    RightParent = Table.addChild("Right Attribute",0,'t');
                                  LeftParent = Table.addChild("Left Attribute",1,'l');
                                       currentParent=LeftParent;
                                       currentRightParent = RightParent;
                                     //break;
                                     TablName = " ";
                                     DummyParent  = currentRightParent.addChild( "dummyparent", xx2,'d' ); 
                                                  currentDummyParent = DummyParent ;
                                                
                                      prvNode = DummyParent;
                                     
                                      tempNode = RightParent.addChild(CelValue, yy2,'t');
                                              System.out.println("error");

                                                firstNextRowChild = tempNode;
                                                prvNode.setNeighbour(tempNode);
                                                System.out.println(" no table name" + " prv: "+ prvNode.data);

                                                prvNode = tempNode;

                                   System.out.println(" first node data :"+tempNode.data +"index:"+tempNode.index + "yy2"+ yy2);

                                }
                                else if( CellPerRow ==1 && yy2 ==0 || leftAtt && CellPerRow ==1 ){
                                      
                                
                                   if (!leftAtt && !secondLeftAtt ){
                                 //     if(leftParentRow != 0)
                                       
                                        secondLeftAtt = true;
                                        prvCelValue = CelValue;
                                        System.out.println("left: ");
                                         currentParent = LeftParent;
                                   
                                    tempNode = currentParent.addChild(CelValue, xx2,'l');
                              System.out.println("first left Attribute"+"\tparent :"+ currentParent.data + "\tdata:"+CelValue);

                               currentLeftParent = tempNode;
                                   }
                                   else if (!leftAtt && secondLeftAtt){
                                        leftAtt = true;
                                      // secondLeftAtt = false;
                                    
                                   
                                    tempNode = currentParent.addChild(CelValue, xx2,'l');
                              System.out.println("second lefttt Attribute"+"\tparent :"+ currentParent.data + "\tdata:"+tempNode.data);

                                  currentLeftParent = tempNode;
                                  System.out.println("currentLeftParent :"+currentLeftParent.data);
                                  // currentParent = tempNode;
                                   }
                           
                                   else{
                                       if (check && xx2 == leftParentRow+1 ){
                                           check = false;
                                           if(currentParent == LeftParent){
                                               System.out.println("xx2 :"+xx2 +"check"+check);
                                        System.out.println("current parent before :"+currentParent.data);
                                        //currentParent = currentParent.parent;
                                        System.out.println("current parent before :"+currentParent.data);
                                    tempNode = currentParent.addChild(strValue, xx2,'l');
                                    currentParent = tempNode;
                                           }
                                           else{
                                             System.out.println("xx2 :"+xx2 +"check"+check);
                                        System.out.println("current parent before :"+currentParent.data);
                                        currentParent = currentParent.parent;
                                        System.out.println("current parent before :"+currentParent.data);
                                    tempNode = currentParent.addChild(strValue, xx2,'l');
                                    currentParent = tempNode;
                                           }
                                       }
                                 tempNode = currentParent.addChild(CelValue, xx2,'l');
                                System.out.println("child left Attribute"+"\tparent :"+ currentParent.data + "\tdata:"+CelValue);
                                      currentLeftParent=  tempNode;
                                   }
                                //  leftAtrrib.add(CelValue);
                                  // Left.data = CelValue;
                                //  Left.childern = CelValue;
                                    temp = CelValue;
                                 }
                                else {
                                    rightAtt = true;
                                    System.out.println("first row  Attribute:");
                                if (!RealfirstRow || firstRowNm == xx2){
                                    RealfirstRow = true;
                                    System.out.println("row number:"+xx2);
                                    currentRightParent =  RightParent;
                                    if (CellPerRow == 1){
                                        firstRowNm = xx2;
                                       DummyParent  = currentRightParent.addChild( "dummyparent", xx2,'d' ); 
                                                        currentDummyParent = DummyParent ;
                                                
                                      prvNode = DummyParent;
                                      Dummy = null;
                                    tempNode = currentRightParent.addChild(CelValue, yy2, 't');
                                      prvNode.setNeighbour(tempNode);
                                    System.out.println("tempNode prv:"+prvNode.data);

                                      prvNode = tempNode;
                                     System.out.println("tempNode parent:"+tempNode.parent.data+"  celValue:"+tempNode.data);

                                    }
                                    else{
                                        tempNode = currentRightParent.addChild(CelValue, yy2, 't');
                                         prvNode.setNeighbour(tempNode);
                                    System.out.println("tempNode prv:"+prvNode.data);

                                      prvNode = tempNode;
                                     System.out.println("tempNode parent:"+tempNode.parent.data+"  celValue:"+tempNode.data);

                                    }
                                }
                                else {
                                   System.out.println(" second row :");

                                     if (CellPerRow ==1 ) {
                                         System.out.println("first cell at second row :");
                                          Dummy  = currentDummyParent.addChild( "dummy", xx2,'d' ); 
                                                   currentDummyParent = Dummy ;
                                             currentRightParent = Dummy.parent.Neighbour; 
                                             prvNode = Dummy;
                                                                                          
                                           if ( yy2 != frColAdress && yy2 == currentRightParent.index ){
                                            System.out.println("not marged: "+currentRightParent.index );

                                           tempNode = currentRightParent.addChild(CelValue, yy2, 't');
                                         prvNode.setNeighbour(tempNode);
                                           System.out.println("tempNode prv:"+prvNode.data);

                                         prvNode =  tempNode;
                                         if( currentRightParent.Neighbour != null )
                                           currentRightParent = currentRightParent.Neighbour;
                                         System.out.println("tempNode parent:"+tempNode.parent.data+"  celValue: "+tempNode.data +"Nighbour: " +currentRightParent.data);
                                        
                                          // System.out.println("tempNode parent:"+tempNode.parent.data+"  celValue:"+tempNode.data);

                                           }
                                           else if (nmOfMgReg >0 && yy2 == currentRightParent.index && yy2 == frColAdress){
                                              System.out.println("marged: "+currentRightParent.index);

                                           tempNode = currentRightParent.addChild(CelValue, yy2, 't');
                                           prvNode.setNeighbour(tempNode);
                                           System.out.println("tempNode prv:"+prvNode.data);

                                             prvNode = tempNode;
                                             System.out.println("tempNode parent:"+tempNode.parent.data+"  celValue:"+tempNode.data);

                                           }
                                           else if (yy2 < currentRightParent.index) {
                                               System.out.println("dummy cell: ");
                                              tempNode =Dummy.parent.addChild(CelValue , yy2,'t');
                                              prvNode.setNeighbour(tempNode);
                                              System.out.println("tempNode prv:"+prvNode.data);
                   
                                              prvNode = tempNode;
                                               System.out.println("tempNode parent:"+tempNode.parent.data+"  celValue:"+tempNode.data);

                                           
                                           }
                                     }
                                     else {
                                         System.out.println("second cell at second row: ");
                                       System.out.println("currentRightParent: "+currentRightParent.data);
                                          
                                           
                                           if (Dummy == null ){
                                          System.out.println("dummyparent have not child:");
                                           Dummy  = currentDummyParent.addChild( "dummy", xx2,'d' ); 
                                                   currentDummyParent = Dummy ;
                                                   currentRightParent = Dummy.parent.Neighbour; 
                                           }

                                         if(  yy2 == currentRightParent.index && (yy2 != frColAdress ||nmOfMgReg ==0 ) ){
                                          System.out.println("not marged cell at second row: ");

                                           if ( secondLeftAtt){
                                         
                                          secondLeftAtt = false;
                                         currentRightParent = Dummy.parent.Neighbour;
                                       tempNode = Dummy.parent.addChild(prvCelValue, yy2,'t');
                                       System.out.println("first Attribute at column 0: "+"\tparent :"+ tempNode.parent.data + "\tdata:"+prvCelValue);
                                          Dummy.setNeighbour(tempNode);
                                            prvNode = tempNode;   
                                           }
                                             
                                         tempNode = currentRightParent.addChild(CelValue, yy2, 't');
                                         prvNode.setNeighbour(tempNode);
                                         System.out.println("tempNode prv:"+prvNode.data);

                                         prvNode =  tempNode;
                                         if (currentRightParent.Neighbour != null)
                                         currentRightParent = currentRightParent.Neighbour;
                                         System.out.println("tempNode parent:"+tempNode.parent.data+"  celValue: "+tempNode.data +" Nighbour: " +currentRightParent.data);
                                        
                                         
                                         }
                                         else if (xx2 == (NmRwAdress+1)&& nmOfMgReg > 0 && NmOfCells >=2 && yy2 <= lstColAdress && yy2 >= frColAdress  ){
                                         System.out.println("marged cell at second row: ");
                                         
                                         if ( secondLeftAtt){
                              
                                          secondLeftAtt = false;
                                         currentRightParent = Dummy.parent.Neighbour;
                                       tempNode = Dummy.parent.addChild(prvCelValue, yy2,'t');
                                       System.out.println("first Attribute at column 0: "+"\tparent :"+ tempNode.parent.data + "\tdata:"+prvCelValue);
                                       Dummy.setNeighbour(tempNode);
                                            prvNode = tempNode;   
                                           }
                                         
                                         tempNode = currentRightParent.addChild(CelValue, yy2, 't');
                                         prvNode.setNeighbour(tempNode);
                                         System.out.println("tempNode prv:"+prvNode.data);

                                         prvNode =  tempNode;
                                         System.out.println("tempNode parent:"+tempNode.parent.data+"  celValue:"+tempNode.data);
                                         if (  yy2 == lstColAdress){
                                           if( currentRightParent.Neighbour != null )
                                         currentRightParent = currentRightParent.Neighbour;
                                                    nmOfMgReg--;
                                                     nmOfMg++;
                                         if (nmOfMgReg > 0 && sheet.getMergedRegion(nmOfMg) != null){
                                         adress =  sheet.getMergedRegion(nmOfMg);
                              
                                        StrAdress = adress.toString();
                                        frColAdress = adress.getFirstColumn();
                                         NmOfCells = adress.getNumberOfCells();
                                         NmRwAdress = adress.getFirstRow();
                                        lstColAdress = adress.getLastColumn();
                                        int lastMgRow = adress.getLastRow();
                                             System.out.println("last row index:"+lstRowNm +" adress as Srting:"+adress.formatAsString());

                              System.out.println("nmOfMg: "+nmOfMg);
                       System.out.println(" Nm regions="+ nmOfMgReg +" \tfirst col of merged:"+frColAdress +" lstColAdress"+lstColAdress+" \tnumber of cells:"+NmOfCells+"\t row:"+NmRwAdress);
                                         }
                                         }
                                         }
                                         else if (yy2 != currentRightParent.index ){
                                         System.out.println("dummy  cell at second row: ");
                                         if ( secondLeftAtt){
                               
                                          secondLeftAtt = false;
                                       currentRightParent = Dummy.parent.Neighbour;
                                       tempNode = Dummy.parent.addChild(prvCelValue, yy2,'t');
                                       System.out.println("first Attribute at column 0: "+"\tparent :"+ tempNode.parent.data + "\tdata:"+prvCelValue);
                                          Dummy.setNeighbour(tempNode);
                                            prvNode = tempNode;   
                                           }
                                         
                                          tempNode =Dummy.parent.addChild(CelValue , yy2,'t');
                                           prvNode.setNeighbour(tempNode);
                                           System.out.println("tempNode prv:"+prvNode.data);
                   
                                           prvNode = tempNode;
                                           System.out.println("tempNode parent:"+tempNode.parent.data+"  celValue:"+tempNode.data);
                                         
                                         }
                                     
                                     
                                     }
                                
                                }
                                 
                                }
                               
                                 }
                            else{
                               // String CelValue = cell.getStringCellValue()
                               System.out.println(" string value:" + " right:"+ rightAtt +" first Rwo :"+FirstRow);
                                if (FirstRow == true){
                                      FirstRow =false;
                                     
                                  if (rightAtt && Dummy == null)
                                      currentRightParent = DummyParent.Neighbour;
                                  else
                                      if (rightAtt) {
                                          currentRightParent = Dummy.Neighbour;
                                      } 
                                 
                                                 /* if (!leftAtt && secondLeftAtt){
                                       
                                                        secondLeftAtt = false;
                                                        currentParent = LeftParent;
                                   
                                                       tempNode = currentParent.addChild(prvCelValue, cell.getRowIndex(),'l');
                                                       System.out.println("first left Attribute"+"\tparent :"+ currentParent.data + "\tdata:"+prvCelValue);

                                                        currentLeftParent = tempNode;
                                                           // currentParent = tempNode;
                                                             }*/
                                                 
                                                     }
                               //System.out.print("string value:"+CelValue);
                               if (currentLeftParent != null){
                                tempNode = currentLeftParent.addChild(CelValue, cell.getRowIndex(),'v');
                                System.out.println("value="+tempNode.data+"\tleft parent:"+currentLeftParent.data);
                                
                               }
                               if (currentRightParent != null){
                                tempNode = currentRightParent.addChild(CelValue, cell.getColumnIndex(),'v');
                                  

                              System.out.print( "value="+tempNode.data+"\t right parent :"+currentRightParent.data );
                               }
                                     if(currentRightParent != null &&currentRightParent.Neighbour != null)
                                         currentRightParent = currentRightParent.Neighbour;
                            }
//                               AttPos[ RealRowsNo][yy2]=true;
                                 //seziof(aaa);
                                 
                               TorF= HeadersQueue.isEmpty();
                      //System.out.println("Attribute:"+" row-"+xx2+" co-"+" "+yy2+" "+CelValue);
			//System.out.print(cell.getStringCellValue() + "\t");
                                                            
							break;
					}
				}
                           // HeadersQueue.add("endRow"); 

				System.out.println("");
                                //lastRow =0;
			}}
                        if (rightAtt )
                        displayTopAtt();
                 
                        displayLeftAtt();
                            displayValue2();
                            displayValue();
                          }while (SecondTable);
                       ;
                         // removeTopAtt();

                        //removeTest();
                          //}while (ct <=1 );
		} 
                          String str = "shhhh";
                          
                         
                         // showLeftParent();
                      // displayLeftAtt();
                       
                        // displayValue();
                        //showLftParnt(str);
                       // showVlue();
                      // showTopAtt();
                       //showValues();
                          

                       // removeTest();
                 }
		catch (Exception e) 
		{
			e.printStackTrace();
		}
        }
   
 public boolean removeTopAtt(){
  Node <String> topAtt, nextAtt, prvParent;
  int i =0;
  if (rightAtt ){
  System.out.println(" ======== remove top Attribute ================");
  topAtt = DummyParent;
  prvParent = RightParent;
  if (Dummy != null){
      System.out.println("dummy = null");
  topAtt = Dummy;
  prvParent = topAtt.parent;
  }
  do {
  while( topAtt != null ){
  System.out.println("top Att: "+topAtt.data );
  topAtt.remove(i);
    System.out.println("top Att child : "+topAtt.getChild(0) );

  topAtt = topAtt.Neighbour ;
  
  }
  if (prvParent == RightParent)
      break ;
  else {
      topAtt =  prvParent;
      if (prvParent.data != RightParent.parent.data && prvParent.parent != RightParent.parent){
      prvParent = prvParent.parent;
//     System.out.println("prvParent: "+prvParent.data);
      }}
     
  } while(topAtt != RightParent ); 
  }
  
      return false;
 }    
 public void removeTest(){
 Node <String> topAtt;

   System.out.println("========= remove ==============");
    topAtt = DummyParent.Neighbour;
   if (Dummy != null)
     topAtt = Dummy.Neighbour;
    
    while (topAtt != null  && topAtt.getChild(0)!= null){
             System.out.println("\ntopAtth:"+topAtt.data);
              topAtt.RemoveAll();
              if (topAtt.getChild(0) != null)
             System.out.println("\ntopAtt Value: "+topAtt.getChild(0).data);
   
             topAtt = topAtt.Neighbour;
        }
   
    
     }
public void showTable(){
 Node <String> pAttNode,AttNode;
 int i =0;
 pAttNode = RightParent;
 while (pAttNode.getChild(0) != null && pAttNode.data != pAttNode.getChild(0).data && pAttNode != firstNextRowChild ){
 System.out.println("pAttNode "+pAttNode.data);
 AttNode=pAttNode.getChild(0);
          
  System.out.println("AttNode "+AttNode.data);
  pAttNode = AttNode;

 while (AttNode.Neighbour != null){
 AttNode=AttNode.Neighbour;
 System.out.println("AttNode "+AttNode.data);
 }
 }
 
    
}
public void showTopAtt(){             // output top Attibute 
    Node <String> topAtt,nextAtt;
    if (rightAtt ){
    nextAtt = DummyParent;
    topAtt = DummyParent.Neighbour;
   if (Dummy != null)
     nextAtt = Dummy.Neighbour;
    do{ 
    while (topAtt != null &&  topAtt.Neighbour != null){
    System.out.println("\ntopAtth:"+topAtt.data);
    if ( topAtt != null && topAtt.Neighbour != null)
    topAtt = topAtt.Neighbour;
      System.out.println("\ntopAtt nighbour:"+topAtt.data);
   
    }
    topAtt = nextAtt;
    System.out.println("topAtt"+topAtt.data);
    if (nextAtt.getChild(0) != null){
    nextAtt = nextAtt.getChild(0);
      System.out.println("nextAtt"+nextAtt.data);
    }
    }while ( nextAtt.data != DummyParent.data && topAtt.c != 'v' );
    }
}


public void showLeftParent(){
   int i =0;
    int k =0;
    int y=0;
    int j =0;
    Node  <String>lParent,vParent,cParent,hParent;
           System.out.println("rlparent :"+LeftParent.data);

   while (LeftParent.getChild(y)!= null && LeftParent.getChild(y).data != LeftParent.data ){
       k =0;
    lParent = LeftParent.getChild(y);
       System.out.println("rlparent :"+lParent.data);
       
       while (lParent.getChild(k)!= null && lParent.getChild(k).data != lParent.data ){
           i =0;
           cParent = lParent.getChild(k);
                  System.out.println("cparent :"+cParent.data);
                 
                  while(cParent.getChild(i)!= null && cParent.getChild(i).data != cParent.data){
                      j =0;
                  vParent = cParent.getChild(i);
                        System.out.println("vparent :"+vParent.data);
                        
                        while (vParent.getChild(j)!= null && vParent.getChild(j).data != vParent.data){
                        hParent = vParent.getChild(j);
                         System.out.println("hparent :"+hParent.data);
                         j++;
                        }
                    i++;
                  }
                 k++;
               }
         y++;
    
    }
    
}
public void showLeftParent_v1(){
    Node  <String>lParent,vParent,cParent,hParent;
    int i =0;
    int k =0;
    int y=0;
    if (LeftParent.getChild(0)!= null ){
        
    lParent = LeftParent.getChild(y);
   
  //  System.out.println("cparent :"+cParent.data);
    do{
         while (lParent.index != lParent.getChild(0).index)
    {
    lParent = lParent.getChild(0);
        System.out.println("rlparent :"+lParent.data);

    }
    cParent =lParent.getChild(0);
    System.out.println("cparent :"+cParent.data);
         
    if(lParent != LeftParent.parent ){
        k =0;
         
        System.out.println("lparent :"+lParent.data);
     System.out.println("cparent :"+cParent.data);
    
    while(cParent.getChild(k) != null && cParent.getChild(k).data != cParent.data   ){
     System.out.println("cparent child ("+k+")"+cParent.getChild(k).data);
    /* hParent =cParent.getChild(k);
     if (hParent.getChild(0) != null && hParent.getChild(0).index != hParent.index ){
         int j =0;
          while(hParent.getChild(k) != null && hParent.getChild(k).data != hParent.data   ){
     System.out.println("hparent child ("+j+")"+hParent.getChild(k).data);
     j++;
          }
     }*/
     k++;
     
    }
    }
    else { 
        i=0;
    cParent = LeftParent;
    while(cParent.getChild(i) != null && cParent.getChild(i).data != cParent.data ){
     System.out.println("cparent child ("+i+")"+cParent.getChild(i).data);
     i++;
    }
    }
    if(cParent != LeftParent &&  cParent.getChild(0)!= null &&cParent.getChild(0).data != cParent.data ){
        System.out.println("bcparent :"+cParent.data);
          cParent= cParent.parent; 
              lParent = cParent;
              System.out.println("hy="+y);
            vParent = cParent.getChild(y+1);
      System.out.println("ulparent :"+lParent.data);

        System.out.println("ucparent :"+cParent.data);
        System.out.println("uvparent :"+vParent.data);
        
         cParent= vParent;
            
    }
    else{
        System.out.println("else");
    lParent = cParent.parent;
    }
 
       y++;
       System.out.println("y"+y);
    }while (cParent.getChild(y) != null && cParent.data != LeftParent.data && lParent.getChild(y).data != lParent.data );
    }
}

public void showValues(){
    
    
   System.out.println("Show Values Function: ");
      System.out.println("============================================= ");


 Node <String> topAtt;
 int i =0;
    if (rightAtt ){
    topAtt = DummyParent.Neighbour;
   if (Dummy != null)
     topAtt = Dummy.Neighbour;
    do {
    while (topAtt != null  && topAtt.getChild(i)!= null){
    System.out.println("\ntopAtth:"+topAtt.data);
        System.out.println("\ntopAtt Value: "+topAtt.getChild(i).data);

  // if (topAtt.Neighbour != null)
   {
       topAtt = topAtt.Neighbour;
      //System.out.println("\ntopAtt nighbour:"+topAtt.data);
   }
    }
    
   if (Dummy != null)
     topAtt = Dummy.Neighbour;
   else 
        topAtt = DummyParent.Neighbour;
    
    
    i ++;
    }while ( topAtt.getChild(i) != null && topAtt.c != 'v' );
    }

}
public void showVlue(){
   
        System.out.println("Show Values Function:=================================================================");

      System.out.println("rightAtt: "+ rightAtt);
       int i =0;
      if (rightAtt){
      topParent = DummyParent.Neighbour;
    if ( Dummy != null ){
    topParent = Dummy.Neighbour;     
    System.out.println("top parent : "+ topParent.data);
    }
    do{
    while (topParent.Neighbour != null ){
     
      // System.out.println("top parent data : "+ topParent.getChild(i).data);

       
       System.out.println("top parent Nighour : "+ topParent.data);
     System.out.println("top parent Nifgbour data : "+ topParent.getChild(i).data);
     topParent = topParent.Neighbour;
   
           }
    if ( Dummy != null ){
    topParent = Dummy.Neighbour;     
    System.out.println("dummy top parent : "+ topParent.data);
    }
    else {      
        topParent = DummyParent;
        System.out.println("top parent : "+ topParent.data);

    }
    i++;
    }while (topParent.getChild(i) != null && topParent.data != topParent.getChild(i).data && topParent.getChild(i).c == 'v');
      }
/*if (firstNextRowChild != null ){
   
    topParent = firstNextRowChild;
   System.out.println("firstNextRowChild:"+firstNextRowChild.data + "\ttopParent"+topParent.data);
   }
   while(topParent!= null){
          int i =0;
while(topParent.getChild(i) != null && topParent.getChild(i).data != topParent.data){
    
    
    System.out.println("current child"+topParent.getChild(i).data + "\t i ="+i );
    
    i++ ;
        }
//if(topParent!= null)
topParent = topParent.Neighbour;
     if(topParent!= null)
System.out.print( "next parents:"+topParent.data);

   }*/

}
public boolean isFstNumeric(String s) {
    int len = s.length();
    char c;
    //for (int i = 0; i < len; ++i) {
    if (len>0)
    {
        c = s.charAt(0);
        if (Character.isDigit(c) ){
            noOfNo++;
        return true;
        
        }
        else
    //}
        {return false;
        }
    }
    else 
        return false;
}    
public boolean Attribute(String str){
         return str.contains("ID") || str.contains("id") || str.contains("ame") || str.contains("ate") || str.contains("able") ;
}
public boolean isAllCapital(String str) {        
    for(int i=str.length()-1; i>=0; i--) {
        if(Character.isLowerCase(str.charAt(i))) {
            return false;
        }
    }
    return true;
}    
}

