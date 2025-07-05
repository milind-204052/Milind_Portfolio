import { useState } from "react";
import { Input } from "@/components/ui/input";
import { Textarea } from "@/components/ui/textarea";
import { Button } from "@/components/ui/button";
import { Card, CardContent } from "@/components/ui/card";
import { Download, UploadCloud, Edit } from "lucide-react";

export default function PortfolioEditor() {
  const [name, setName] = useState("Milind Baranwal");
  const [title, setTitle] = useState("Experienced Program Manager");
  const [summary, setSummary] = useState(
    "Led $500M global digital transformation portfolio across Fortune 500 firms. Expertise in Agile, ERP, CRM, automation, and strategic initiatives across US & Europe."
  );
  const photo = "/mnt/data/DSC_4642.JPG";
  const resume = "/mnt/data/Milind_Baranwal.pdf";

  return (
    <div className="max-w-5xl mx-auto p-6 space-y-6">
      <Card className="shadow-xl">
        <CardContent className="p-6 space-y-6">
          <div className="flex items-center gap-6">
            <img src={photo} alt="Milind Baranwal" className="w-28 h-28 rounded-full object-cover border" />
            <div>
              <h1 className="text-2xl font-bold">{name}</h1>
              <h2 className="text-lg text-gray-600">{title}</h2>
              <a href={resume} download className="text-sm text-blue-600 inline-flex items-center mt-2">
                <Download className="w-4 h-4 mr-1" /> Download Resume
              </a>
            </div>
          </div>

          <div>
            <h3 className="text-lg font-semibold">Summary</h3>
            <p className="text-sm text-gray-700 leading-relaxed">{summary}</p>
          </div>

          <div>
            <h3 className="text-lg font-semibold">Certifications</h3>
            <ul className="list-disc list-inside text-sm text-gray-700">
              <li>Project Management Professional (PMP)</li>
              <li>Certified Scrum Master (CSM)</li>
              <li>Lean Six Sigma Green Belt (KPMG)</li>
            </ul>
          </div>

          <div>
            <h3 className="text-lg font-semibold">Technical Skills</h3>
            <ul className="list-disc list-inside text-sm text-gray-700">
              <li>Project Tools: MS Project, SharePoint, Jira, Confluence</li>
              <li>ERP: Oracle Fusion Cloud, SAP ECC</li>
              <li>CRM: Salesforce</li>
              <li>Analytics: Power BI, SQL, Excel, R Studio, Python</li>
              <li>Soft Skills: Stakeholder Management, Risk Management, Change Management</li>
            </ul>
          </div>

          <div>
            <h3 className="text-lg font-semibold">Experience</h3>
            <div className="space-y-4">
              <div>
                <h4 className="font-medium">Dover Corporation (Jan 2022 – Apr 2025)</h4>
                <p className="text-sm text-gray-700">Program Manager – Digital Transformation</p>
                <ul className="list-disc list-inside text-sm text-gray-700">
                  <li>Saved $240K by automating global billing system using ARIA RPA.</li>
                  <li>Led Oracle ERP rollout across 7 divisions, increasing sales by 60%.</li>
                  <li>Reduced false warranty claims by 43% via Salesforce enhancements.</li>
                  <li>Saved $150K launching PCI-compliant PayTrace payment gateway.</li>
                  <li>Delivered PIM project managing 65,000 digital assets ($1.8M valuation).</li>
                </ul>
              </div>
              <div>
                <h4 className="font-medium">OLA Cabs (May 2021 – Jan 2022)</h4>
                <p className="text-sm text-gray-700">Project Manager – Strategic Initiatives</p>
                <ul className="list-disc list-inside text-sm text-gray-700">
                  <li>Expanded Bike Taxis to 90 cities, boosting revenue by 10%.</li>
                  <li>Achieved 80% vaccinated driver rides, enhancing rider trust.</li>
                  <li>Executed delivery of 770 oxygen concentrators across India.</li>
                </ul>
              </div>
              <div>
                <h4 className="font-medium">Reliance Industries (Oct 2012 – Jan 2019)</h4>
                <p className="text-sm text-gray-700">Manager – Planning</p>
                <ul className="list-disc list-inside text-sm text-gray-700">
                  <li>Led ₹510 Cr EPC project, managing electrical systems commissioning.</li>
                  <li>Saved ₹5 Cr through SAP ERP (ECC PM/MM) implementation.</li>
                  <li>Streamlined operations saving ₹3.5 lakhs and 400+ man-hours.</li>
                </ul>
              </div>
            </div>
          </div>

          <div>
            <h3 className="text-lg font-semibold">Education</h3>
            <ul className="list-disc list-inside text-sm text-gray-700">
              <li>PGPM – Operations & Analytics, Great Lakes Institute of Management (2019–20)</li>
              <li>B.Tech – Electrical Engineering, NIT Raipur (2008–12)</li>
            </ul>
          </div>

          <div className="text-right">
            <Button>
              <Edit className="w-4 h-4 mr-2" /> Edit Portfolio
            </Button>
          </div>
        </CardContent>
      </Card>
    </div>
  );
}
