import React, { useState } from 'react';
import { Upload, Split, Sparkles, Send, ArrowLeft, ArrowRight } from 'lucide-react';

// Define the steps of the campaign creation flow
const STEPS = [
  { id: 1, name: 'Upload Data', icon: Upload, description: 'Customer transaction CSV file.' },
  { id: 2, name: 'Segmentation', icon: Split, description: 'RFM/CLV analysis and segment review.' },
  { id: 3, name: 'Generate Content', icon: Sparkles, description: 'AI-powered copy generation.' },
  { id: 4, name: 'Review & Send', icon: Send, description: 'Final review and campaign scheduling.' },
];

/**
 * Placeholder component for Step 1: Upload Data
 */
const UploadDataStep = () => (
  <div className="space-y-4">
    <h2 className="text-2xl font-semibold text-gray-800">1. Upload Customer Data</h2>
    <p className="text-gray-600">Securely upload your customer transaction history CSV file here. The system will automatically detect necessary fields like Customer ID, Recency, Frequency, and Monetary Value.</p>
    <div className="p-6 border-2 border-dashed border-indigo-300 rounded-xl bg-indigo-50 hover:bg-indigo-100 transition duration-150 cursor-pointer">
      <div className="text-center">
        <Upload className="w-8 h-8 mx-auto text-indigo-500" />
        <p className="mt-2 text-sm font-medium text-indigo-600">Drag & drop your CSV file or click to browse</p>
        <p className="text-xs text-gray-500">Max file size 10MB (.csv only)</p>
      </div>
    </div>
    <div className="mt-4 p-3 bg-yellow-100 border border-yellow-300 rounded-lg text-sm text-yellow-800">
      ⚠️ **Placeholder:** Data will be processed by Python/Pandas backend logic upon real upload.
    </div>
  </div>
);

/**
 * Placeholder component for Step 2: Segmentation (Updated with 3 Segments)
 */
const SegmentationStep = () => (
  <div className="space-y-4">
    <h2 className="text-2xl font-semibold text-gray-800">2. Review Customer Segmentation</h2>
    <p className="text-gray-600">The RFM analysis is complete. Review the three automatically generated customer segments before generating targeted copy.</p>
    
    {/* Updated grid layout for 3 segments */}
    <div className="grid gap-4 sm:grid-cols-2 lg:grid-cols-3">
      {[
        { title: "High Value", count: 180, color: "bg-green-500", desc: "Top spenders with high frequency and recency." },
        { title: "Mid Value", count: 450, color: "bg-blue-500", desc: "Consistent buyers with moderate spend." },
        { title: "Low Value", count: 100, color: "bg-red-500", desc: "Infrequent buyers or low average order value." },
      ].map((segment, index) => (
        <div key={index} className="p-4 rounded-xl shadow-lg border border-gray-100">
          <div className={`w-8 h-1 ${segment.color} rounded mb-2`}></div>
          <h3 className="text-lg font-bold text-gray-900">{segment.title}</h3>
          <p className="text-3xl font-extrabold text-gray-700">{segment.count}</p>
          <p className="text-sm text-gray-500">{segment.desc}</p>
        </div>
      ))}
    </div>
    <div className="mt-4 p-3 bg-yellow-100 border border-yellow-300 rounded-lg text-sm text-yellow-800">
      ⚠️ **Placeholder:** This data will be dynamically loaded from the Python RFM calculations.
    </div>
  </div>
);

/**
 * Placeholder component for Step 3: Generate Content
 */
const GenerateContentStep = () => {
    // Segments updated to reflect the new three types
    const segments = ["High Value", "Mid Value", "Low Value"];
    const platforms = ["Email", "WhatsApp"];

    return (
      <div className="space-y-6">
        <h2 className="text-2xl font-semibold text-gray-800">3. Generate AI Copy</h2>
        <p className="text-gray-600">Use the Gemini API to instantly create tailored messaging for each segment and platform, ensuring maximum personalization.</p>

        <div className="grid gap-6 md:grid-cols-2">
            {platforms.map(platform => (
                <div key={platform} className="p-5 border border-gray-200 rounded-xl shadow-sm bg-white">
                    <h3 className="text-xl font-bold text-indigo-700 mb-4">{platform} Copy</h3>
                    {segments.map(segment => (
                        <div key={segment} className="mb-4 p-3 bg-indigo-50 rounded-lg border border-indigo-200">
                            <h4 className="font-semibold text-indigo-800">{segment} Segment</h4>
                            <p className="text-sm text-gray-700 italic">"Hey [Customer Name], we've tailored this message just for our **{segment}** customers..."</p>
                        </div>
                    ))}
                </div>
            ))}
        </div>

        <button
          className="w-full md:w-auto px-6 py-3 bg-indigo-600 text-white font-bold rounded-xl shadow-lg hover:bg-indigo-700 transition duration-200 flex items-center justify-center space-x-2"
          onClick={() => console.log('Simulating Gemini API call...')}
        >
          <Sparkles className="w-5 h-5"/>
          <span>Generate AI Content Now</span>
        </button>

        <div className="mt-4 p-3 bg-yellow-100 border border-yellow-300 rounded-lg text-sm text-yellow-800">
          ⚠️ **Placeholder:** This step will contain the API logic to call the Gemini model.
        </div>
      </div>
    );
};

/**
 * Placeholder component for Step 4: Review & Send
 */
const ReviewAndSendStep = () => (
  <div className="space-y-4">
    <h2 className="text-2xl font-semibold text-gray-800">4. Review & Launch Campaign</h2>
    <p className="text-gray-600">Final check of the generated content and configuration before sending the campaigns via Mailchimp and Twilio/WhatsApp Business API.</p>

    <div className="grid gap-4 md:grid-cols-2">
      <div className="p-5 border border-green-200 rounded-xl bg-green-50">
        <h3 className="font-bold text-green-700">Email (Mailchimp) Status</h3>
        <p className="text-sm text-gray-700">Status: Ready to send to 730 contacts.</p>
        <p className="text-xs text-gray-500 mt-2">API Connection: Established (Mailchimp Key connected)</p>
      </div>
      <div className="p-5 border border-green-200 rounded-xl bg-green-50">
        <h3 className="font-bold text-green-700">WhatsApp (Twilio) Status</h3>
        <p className="text-sm text-gray-700">Status: Ready to send to 250 contacts (opt-in).</p>
        <p className="text-xs text-gray-500 mt-2">API Connection: Established (Twilio Key connected)</p>
      </div>
    </div>

    <button
      className="w-full px-8 py-4 bg-lime-600 text-white font-extrabold text-lg rounded-xl shadow-xl hover:bg-lime-700 transition duration-200 flex items-center justify-center space-x-2 mt-6"
      onClick={() => console.log('Campaign Scheduled!')}
    >
      <Send className="w-6 h-6"/>
      <span>Schedule & Launch Campaign</span>
    </button>
  </div>
);


/**
 * Main Application Component (Flow Dashboard)
 */
const App = () => {
  const [currentStep, setCurrentStep] = useState(1);

  const totalSteps = STEPS.length;

  const navigateToStep = (stepId) => {
    if (stepId >= 1 && stepId <= totalSteps) {
      setCurrentStep(stepId);
    }
  };

  const nextStep = () => {
    navigateToStep(currentStep + 1);
  };

  const prevStep = () => {
    navigateToStep(currentStep - 1);
  };

  const renderStepContent = () => {
    switch (currentStep) {
      case 1:
        return <UploadDataStep />;
      case 2:
        return <SegmentationStep />;
      case 3:
        return <GenerateContentStep />;
      case 4:
        return <ReviewAndSendStep />;
      default:
        return <UploadDataStep />;
    }
  };

  const StepIndicator = ({ step, isActive, isComplete }) => {
    const Icon = step.icon;
    
    let containerClasses = "flex items-center space-x-3 p-3 rounded-xl transition duration-300 ";
    let iconClasses = "w-6 h-6 ";
    let textClasses = "font-medium ";

    if (isActive) {
      containerClasses += "bg-indigo-100 ring-2 ring-indigo-500 shadow-md";
      iconClasses += "text-indigo-600";
      textClasses += "text-indigo-700 font-bold";
    } else if (isComplete) {
      containerClasses += "bg-white hover:bg-gray-50 cursor-pointer";
      iconClasses += "text-green-500";
      textClasses += "text-gray-600";
    } else {
      containerClasses += "bg-white hover:bg-gray-50 cursor-pointer opacity-70";
      iconClasses += "text-gray-400";
      textClasses += "text-gray-500";
    }

    return (
      <div 
        className={containerClasses}
        onClick={() => navigateToStep(step.id)}
      >
        <div className={`p-2 rounded-full ${isActive ? 'bg-indigo-500 text-white' : 'bg-gray-100 text-gray-500'}`}>
            <Icon className="w-4 h-4" />
        </div>
        <div className='flex-1 hidden md:block'>
          <p className="text-xs text-gray-500">STEP {step.id}</p>
          <p className={textClasses}>{step.name}</p>
        </div>
      </div>
    );
  };

  return (
    <div className="min-h-screen bg-gray-50 font-sans p-4 md:p-8">
      <div className="max-w-6xl mx-auto">
        <header className="mb-8">
          <h1 className="text-3xl font-extrabold text-gray-900">
            Create New Marketing Campaign
          </h1>
          <p className="text-gray-500 mt-1">
            Follow the 4-step flow to segment your customers and generate personalized copy.
          </p>
        </header>

        {/* Campaign Flow Stepper */}
        <div className="bg-white p-4 mb-8 shadow-xl rounded-2xl border border-gray-100">
          <div className="flex justify-between space-x-2 md:space-x-4">
            {STEPS.map((step) => (
              <div key={step.id} className="flex-1 min-w-0">
                <StepIndicator
                  step={step}
                  isActive={currentStep === step.id}
                  isComplete={currentStep > step.id}
                />
              </div>
            ))}
          </div>
        </div>

        {/* Main Content Area */}
        <div className="bg-white p-6 md:p-10 shadow-xl rounded-2xl border border-gray-100">
          {renderStepContent()}
        </div>

        {/* Navigation Controls */}
        <div className="mt-8 flex justify-between p-4 bg-white rounded-2xl shadow-lg border border-gray-100">
          <button
            onClick={prevStep}
            disabled={currentStep === 1}
            className={`px-6 py-3 rounded-xl font-semibold transition duration-200 flex items-center space-x-2 ${
              currentStep === 1
                ? 'bg-gray-200 text-gray-500 cursor-not-allowed'
                : 'bg-indigo-500 text-white hover:bg-indigo-600 shadow-md'
            }`}
          >
            <ArrowLeft className="w-5 h-5" />
            <span>Previous Step</span>
          </button>

          <button
            onClick={nextStep}
            disabled={currentStep === totalSteps}
            className={`px-6 py-3 rounded-xl font-semibold transition duration-200 flex items-center space-x-2 ${
              currentStep === totalSteps
                ? 'bg-lime-200 text-lime-700 cursor-not-allowed'
                : 'bg-indigo-500 text-white hover:bg-indigo-600 shadow-md'
            }`}
          >
            <span>{currentStep === totalSteps - 1 ? 'Go to Review' : 'Next Step'}</span>
            <ArrowRight className="w-5 h-5" />
          </button>
        </div>
      </div>
    </div>
  );
};

export default App;

