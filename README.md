
import java.io.File;
import java.io.FileInputStream;
import java.io.FileOutputStream;
import javax.swing.JFileChooser;
import javax.swing.JOptionPane;

/*
 * Click nbfs://nbhost/SystemFileSystem/Templates/Licenses/license-default.txt to change this license
 * Click nbfs://nbhost/SystemFileSystem/Templates/GUIForms/JFrame.java to edit this template
 */

/**
 *
 * @author nikit
 */
public class Photos extends javax.swing.JFrame {

    /**
     * Creates new form Photos
     */
    public Photos() {
        initComponents();
        setExtendedState(javax.swing.JFrame.MAXIMIZED_BOTH);
    }
    public void operate1(){
        /*JFileChooser fileChooser=new JFileChooser();
         fileChooser.showOpenDialog(null);
         File f= fileChooser.getSelectedFile();
         file_path.setText(f.getAbsolutePath());
         fp=f;*/
    
    }
    public void operate(int key){
    try{
            FileInputStream fis=new FileInputStream(fp);
            byte[]data=new byte[fis.available()];
            fis.read(data);
            int i=0;
            for(byte b:data)
            {
                data[i]=(byte)(b^key);
                i++;
            }

            FileOutputStream fos=new FileOutputStream(fp);
            fos.write(data);
            fos.close();
            fis.close();


        }
        catch(Exception e){
         JOptionPane.showMessageDialog(null,"SOMETHING WENT WRONG");
        }
    }

    @SuppressWarnings("unchecked")
    // <editor-fold defaultstate="collapsed" desc="Generated Code">                          
    private void initComponents() {

        jFrame1 = new javax.swing.JFrame();
        jPanel1 = new javax.swing.JPanel();
        file_path = new javax.swing.JTextField();
        jButton2 = new javax.swing.JButton();
        jButton3 = new javax.swing.JButton();
        jButton1 = new javax.swing.JButton();
        jButton4 = new javax.swing.JButton();
        jTextField1 = new javax.swing.JTextField();
        jLabel2 = new javax.swing.JLabel();
        jLabel1 = new javax.swing.JLabel();

        javax.swing.GroupLayout jFrame1Layout = new javax.swing.GroupLayout(jFrame1.getContentPane());
        jFrame1.getContentPane().setLayout(jFrame1Layout);
        jFrame1Layout.setHorizontalGroup(
            jFrame1Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGap(0, 400, Short.MAX_VALUE)
        );
        jFrame1Layout.setVerticalGroup(
            jFrame1Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGap(0, 300, Short.MAX_VALUE)
        );

        setDefaultCloseOperation(javax.swing.WindowConstants.EXIT_ON_CLOSE);
        setBackground(new java.awt.Color(204, 204, 204));
        getContentPane().setLayout(new org.netbeans.lib.awtextra.AbsoluteLayout());

        jPanel1.setBackground(new java.awt.Color(204, 204, 204));
        jPanel1.setBorder(javax.swing.BorderFactory.createMatteBorder(15, 15, 15, 15, new java.awt.Color(51, 102, 255)));

        file_path.setFont(new java.awt.Font("Segoe UI", 1, 14)); // NOI18N
        file_path.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                file_pathActionPerformed(evt);
            }
        });

        jButton2.setBackground(new java.awt.Color(153, 153, 153));
        jButton2.setFont(new java.awt.Font("Segoe UI", 1, 18)); // NOI18N
        jButton2.setText("HIDE");
        jButton2.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                jButton2ActionPerformed(evt);
            }
        });

        jButton3.setBackground(new java.awt.Color(153, 153, 153));
        jButton3.setFont(new java.awt.Font("Segoe UI", 1, 18)); // NOI18N
        jButton3.setText("UNHIDE");
        jButton3.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                jButton3ActionPerformed(evt);
            }
        });

        jButton1.setBackground(new java.awt.Color(153, 153, 153));
        jButton1.setFont(new java.awt.Font("Segoe UI", 1, 18)); // NOI18N
        jButton1.setText("SELECT");
        jButton1.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                jButton1ActionPerformed(evt);
            }
        });

        jButton4.setBackground(new java.awt.Color(153, 153, 153));
        jButton4.setFont(new java.awt.Font("Segoe UI", 1, 18)); // NOI18N
        jButton4.setText("BACK");
        jButton4.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                jButton4ActionPerformed(evt);
            }
        });

        jTextField1.setFont(new java.awt.Font("Segoe UI", 1, 14)); // NOI18N
        jTextField1.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                jTextField1ActionPerformed(evt);
            }
        });

        jLabel2.setFont(new java.awt.Font("Segoe UI", 1, 14)); // NOI18N
        jLabel2.setText("Enter key:");

        javax.swing.GroupLayout jPanel1Layout = new javax.swing.GroupLayout(jPanel1);
        jPanel1.setLayout(jPanel1Layout);
        jPanel1Layout.setHorizontalGroup(
            jPanel1Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(jPanel1Layout.createSequentialGroup()
                .addContainerGap(122, Short.MAX_VALUE)
                .addGroup(jPanel1Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                    .addGroup(jPanel1Layout.createSequentialGroup()
                        .addComponent(jButton4)
                        .addGap(134, 134, 134)
                        .addComponent(jButton2, javax.swing.GroupLayout.PREFERRED_SIZE, 102, javax.swing.GroupLayout.PREFERRED_SIZE)
                        .addGap(76, 76, 76)
                        .addComponent(jButton3))
                    .addGroup(jPanel1Layout.createSequentialGroup()
                        .addGroup(jPanel1Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.TRAILING)
                            .addGroup(jPanel1Layout.createSequentialGroup()
                                .addComponent(jLabel2, javax.swing.GroupLayout.PREFERRED_SIZE, 76, javax.swing.GroupLayout.PREFERRED_SIZE)
                                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                                .addComponent(jTextField1, javax.swing.GroupLayout.PREFERRED_SIZE, 243, javax.swing.GroupLayout.PREFERRED_SIZE)
                                .addGap(46, 46, 46))
                            .addComponent(file_path, javax.swing.GroupLayout.PREFERRED_SIZE, 427, javax.swing.GroupLayout.PREFERRED_SIZE))
                        .addGap(57, 57, 57)
                        .addComponent(jButton1, javax.swing.GroupLayout.PREFERRED_SIZE, 98, javax.swing.GroupLayout.PREFERRED_SIZE)))
                .addGap(0, 97, Short.MAX_VALUE))
        );
        jPanel1Layout.setVerticalGroup(
            jPanel1Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(jPanel1Layout.createSequentialGroup()
                .addGroup(jPanel1Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.TRAILING)
                    .addGroup(jPanel1Layout.createSequentialGroup()
                        .addGap(74, 74, 74)
                        .addComponent(jButton1, javax.swing.GroupLayout.PREFERRED_SIZE, 33, javax.swing.GroupLayout.PREFERRED_SIZE)
                        .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE))
                    .addGroup(jPanel1Layout.createSequentialGroup()
                        .addGap(25, 25, 25)
                        .addGroup(jPanel1Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                            .addComponent(jTextField1, javax.swing.GroupLayout.PREFERRED_SIZE, 33, javax.swing.GroupLayout.PREFERRED_SIZE)
                            .addComponent(jLabel2))
                        .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED, 27, Short.MAX_VALUE)
                        .addComponent(file_path, javax.swing.GroupLayout.PREFERRED_SIZE, 33, javax.swing.GroupLayout.PREFERRED_SIZE)
                        .addGap(66, 66, 66)))
                .addGroup(jPanel1Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    .addComponent(jButton2)
                    .addComponent(jButton3)
                    .addComponent(jButton4))
                .addGap(45, 45, 45))
        );

        getContentPane().add(jPanel1, new org.netbeans.lib.awtextra.AbsoluteConstraints(280, 310, -1, 290));

        jLabel1.setIcon(new javax.swing.ImageIcon("C:\\Users\\nikit\\OneDrive\\Pictures\\whatsapp images\\newlock.png")); // NOI18N
        getContentPane().add(jLabel1, new org.netbeans.lib.awtextra.AbsoluteConstraints(0, 0, 1690, 850));

        pack();
    }// </editor-fold>                        

    private void file_pathActionPerformed(java.awt.event.ActionEvent evt) {                                          
        // TODO add your handling code here:
    }                                         

    private void jButton1ActionPerformed(java.awt.event.ActionEvent evt) {                                         
         JFileChooser fileChooser=new JFileChooser();
         fileChooser.showOpenDialog(null);
         File f= fileChooser.getSelectedFile();
         file_path.setText(f.getAbsolutePath());
         fp=f;
           //operate1();
        
    }                                        

    private void jButton2ActionPerformed(java.awt.event.ActionEvent evt) {                                         
        // TODO add your handling code here:
        String text= jTextField1.getText();
           int temp=Integer.parseInt(text);
           operate(temp);
           JOptionPane.showMessageDialog(null,"HIDDEN SUCCESSFULLY");

    }                                        

    private void jButton4ActionPerformed(java.awt.event.ActionEvent evt) {                                         
        // TODO add your handling code here:
        Mainmenu mn=new Mainmenu();
        mn.setVisible(true);
        this.setVisible(false);
    }                                        

    private void jButton3ActionPerformed(java.awt.event.ActionEvent evt) {                                         
           String text= jTextField1.getText();
           int temp=Integer.parseInt(text);
           operate(temp);
           JOptionPane.showMessageDialog(null,"DONE");
    
    }                                        

    private void jTextField1ActionPerformed(java.awt.event.ActionEvent evt) {                                            
        // TODO add your handling code here:
    }                                           

File fp;


    // Variables declaration - do not modify                     
    private javax.swing.JTextField file_path;
    private javax.swing.JButton jButton1;
    private javax.swing.JButton jButton2;
    private javax.swing.JButton jButton3;
    private javax.swing.JButton jButton4;
    private javax.swing.JFrame jFrame1;
    private javax.swing.JLabel jLabel1;
    private javax.swing.JLabel jLabel2;
    private javax.swing.JPanel jPanel1;
    private javax.swing.JTextField jTextField1;
    // End of variables declaration                   
}
