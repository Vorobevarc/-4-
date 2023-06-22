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
            textBox7.Text = "";
        }

        private void button1_Click(object sender, EventArgs e)
        {
            double p = double.Parse(textBox4.Text);
            textBox6.Text += Environment.NewLine +"p = " + p.ToString();
            double q = double.Parse(textBox5.Text);
            textBox6.Text += Environment.NewLine + "q = " + q.ToString();
            double n = Math.Abs(p * q);
            textBox6.Text += Environment.NewLine + "n = " + n.ToString();
            double fi = Math.Abs((p - 1) * (q - 1));
            textBox6.Text += Environment.NewLine + "fi = " + fi.ToString();

        }
        private void button2_Click(object sender, EventArgs e)
        {

        }
    }
}
