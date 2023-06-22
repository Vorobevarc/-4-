using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace WindowsFormsApp2
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }

        private void Form1_Load(object sender, EventArgs e)
        {
            textBox4.Text = "";
            textBox5.Text = "";
        }

        private void button1_Click(object sender, EventArgs e)
        {
            int p = int.Parse(textBox4.Text);
            textBox6.Text += Environment.NewLine +"p = " + p.ToString();
            int q = int.Parse(textBox5.Text);
            textBox6.Text += Environment.NewLine + "q = " + q.ToString();
            int n = Math.Abs(p * q);
            textBox8.Text += Environment.NewLine + n.ToString();
            int fi = Math.Abs((p - 1) * (q - 1));
            textBox6.Text += Environment.NewLine + "fi = " + fi.ToString();
            
        }
    }
}
